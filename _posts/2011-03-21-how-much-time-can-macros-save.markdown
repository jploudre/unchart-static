---
author: jploudre
comments: false
date: 2011-03-21 02:42:30+00:00
layout: post
slug: how-much-time-can-macros-save
title: How much time can Macros Save?
wordpress_id: 517
categories:
- software
- theory
tags:
- autohotkey
- efficiency
- macro
---

In the background of my computer, I've been tracking my work lately -- at a very low level. How many mouseclicks? How many characters typed? Honestly, sometimes it feels like that's my job description. 

I've been using Autohotkey for macros and abbreviations for most of the 3 years I have used e-MDs. I've got dozens of macros, and hundreds-to-thousands of abbreviations/typo corrections. How much time does all that macroing save?

My estimates are based on a model of how users generally use computers (Wikipedia: [Keystroke Level Model](http://en.wikipedia.org/wiki/Keystroke-Level_Model)). Your mileage will vary.

### A typical month's worth of work
|Activity|#|Time|
|-------|--------|--------|
|Typing|127K characters|10.6 hours|
|Mouseclicking|32K clicks|9.1 hours|

### Savings

|Activity|#|Time|
|-------|--------|--------|
|Typing|24K characters.|2 hours|
|Mouseclicking|5K clicks|1.5 hours|

The time saved on clicking is probably much more given some macros save 30 seconds. For example, consider labs in order tracking. For planned care visits (checkups, diabetes, hypertension, etc), I have a macro that notes 'Will discuss...', signs it off, removes it from ordertracking. Every day I use it a couple times and it saves me about a minute of documentation. Improves my record-keeping, reduces my stress.

	; Planned Care Lab. Annotes a lab to Discuss, signs, removes from order tracking
	^+p::
	IfWinActive, Patient Chart
	{
	click, 915, 150
	WinWaitActive, Memo
	Sleep, 200
	SendInput, Discuss at already scheduled 'planned-care' visit.
	click, 435, 439
	WinWaitActive, Patient Chart
	{
	sleep, 200
	click, 854, 150
	sleep, 200
	click, 51, 182
	sleep 200
	click, 70, 259
	sleep, 200
	Send !fx
	}
	}
	return

So using my low level data as a family doctor, generally living in e-MDs all day long: I've got more than 1 hour straight clicking/typing per typical workday. And Macros/Abbreviations save me about 15% of the typing/clicking. That's probably my limit because most months are about the same. It's a local maximum for me. I can write more macros but I won't get that much improvement

![](/files/2011/03/local-maximum.gif)

The [Local Maximum](http://52weeksofux.com/post/694598769/the-local-maximum) is a key concept. You can only *optimize* so far. Sometimes you need to *redesign*. This applies macros, or to practice processes or graphic design.

So unless the situation changes (say, Meaningful Use changing workflows and adding clicking), I'm only going to get so far with macros and abbreviations. I'll still use them a lot partly because they work well with my style. But if I really want to get done quicker, I either need to decrease quantity (type and click less), increase speed (probably not going to help much), or change method (Dragon Naturally Speaking, better templates, better delegation, hire a scribe, et cetera.)
