---
author: jploudre
comments: false
date: 2011-02-23 22:21:39+00:00
layout: post
slug: macro-to-add-flowsheets-in-e-mds
title: Macro to add flowsheets in e-MDs
wordpress_id: 452
categories:
- software
tags:
- autohotkey
- e-MDs
- macro
- proofofconcept
---

In our clinic we wanted to use vitals flowsheets but they were turned on in most charts. We have about 15K patients. So if it takes 15 seconds to open a chart and turn it on, you've got 62 hours of mindless clicking for someone to do.

e-MDs has a script (SQL) with this functionality but we couldn't get it (it's unofficial/unsupported.)

[Autohotkey ](http://autohotkey.com)to the rescue!

I wrote a brief script to loop through account numbers and do it. I suspect there's a memory leak in e-MDs because this would repeatedly crash (different ways, slightly different frequency) about every 120 patients. Still, it made the process about 20x faster in hands on time. This does about 10 patients a minute. It could go faster but our e-MDs performance is pretty variable on 'snappiness'.

Here's the source code, and you'd need a file with account numbers (that'd be a separate task, obviously.)

----

    DetectHiddenText, Off
    
    ; Loop through a list of Account Numbers and turn on vitals flowsheet.
    ; Hit F7 in Chart to start. Needs a file named ptlist.ttx (made with a report, 
    ; limited to a single column of account numbers.
    
    F7::
    Loop, Read, ptlist.ttx
    {
    Send !fo
    WinWaitActive, Find Chart Patient
    ControlFocus, TrscEdit6
    ; Enter the Account Number
    Send %A_LoopReadLine%
    Send !s{Enter}
	; Needs a longish delay since patient alerts can be slow to pop up.
	sleep, 2000
	Ifwinactive, Patient Alert
	Send !s
    WinWaitActive, e-MDs Chart
    sleep, 500
    ; Open Flowsheets, Wait for it to be active.
    Send !l
    WinGetText wintext
    While (IfNotInString, wintext, pcsFlowSheets)
	{
	sleep, 100
	}
    sleep, 200
    Click, 21, 155
    WinWaitActive, FlowSheet Select
    Send Vital{Enter}{Enter}
    ; If duplicate flowsheet, 'enter' through.
    sleep, 1000
    Send {Enter}
    Click, 330, 60
    sleep, 1000
    }

