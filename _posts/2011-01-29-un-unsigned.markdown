---
author: jploudre
comments: true
date: 2011-01-29 18:01:28+00:00
layout: post
slug: un-unsigned
title: Un-Unsigned
wordpress_id: 292
categories:
- software
tags:
- crystalreport
- e-MDs
- efficiency
- macro
- mistakeproof
---

Much e-MDs is focused on visits to the doctor. (Chart, Bill, Schedule). But it also  has panel-managment tools like Order Tracking, Refills, Unsigned Notes. These let you at a glance see how your practice is doing overall.

**Un-Unsigned** is a panel management tool for making sure that you're signing off the thousands of documents that come your way. It helps you mistake-proof against things being mishandled. It automates flipping through unsigned scans and labs.

In the standard e-MDs report, there are many documents that may never need to be signed off (administrative forms, etc.) And it's a serious drain on your energy to open up each person's  account so you can find the document to sign off. On my **Un-Unsigned**, there's a custom crystal report (which may need to be customized for your practice). In our practice, the report eliminates many faxes and financial forms, for example.



#### Installing Un-Unsigned

There are multi-step instructions included in the zip. Directions assume familiarity with e-MDs and some of the technical bits. 

#### Using Un-Unsigned

1. Tip: Clear out taskman and order tracking first.
1. Open the app
2. Go into e-MDs
4. Hit F5 to collect your unsigned documents (takes about a half minute)
5. Hit F1 for the next document
6. Learning/Using the keyboard shortcuts in the macro will make you quicker over time.

[![](/files/2011/01/57-download.png) Un-Unsigned.zip](http://unchart.com/notes/images/Un-Unsigned.zip "Un-Unsigned")

* **Known Issue 1** In my clinic, computers have different installs (say, no Bill) so that causes problems for the macro. Wifi problems can also cause it to crash. I could make it more resilient by slowing it down but that degrades it for me personally since I like having it run quickly. I do have a few partners who use this regularly.
* **Known Issue 2** This includes documents assigned to me. But sometimes the reason it is unsigned was that it wasn't assigned to me. I plan to add a patient-centered report (my patients, documents that are unsigned whether they are mine to sign or not.)
* **Tested on:** e-MDs 6.32
