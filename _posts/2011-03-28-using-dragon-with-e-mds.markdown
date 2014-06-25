---
author: jploudre
comments: false
date: 2011-03-28 01:12:15+00:00
layout: post
slug: using-dragon-with-e-mds
title: Using (Not Just Medical) Dragon with e-MDs
wordpress_id: 544
categories:
- software
- theory
tags:
- abbreviation
- dragon
- e-MDs
- efficiency
- macro
- usability
---

Voice Recognition has been just around the corner for at least 5 years. My clinic has a number of docs who've been pretty sucessful over the years. We bought Dragon Professional years ago and spent some *serious cash* on some Medical Vocabularies. I've tried it repeatedly over the years but my dictation is pretty error-prone and frustrating. I get motivated for a while and then lose steam a week or two later. Anyone who's read any of this site will know: I use the keyboard (with macros and abbreviations galore.)

But I've hit a [local maximum](/2011/how-much-time-can-macros-save/) and more macros/abbreviations won't really save me time. If I try to re-design my workflow for speed, I need better ways of doing 2 things.

1. I need faster [narrative medicine](/2011/snappy-charting/) so I can put more flavor into my notes. Plain templates makes for pretty bland notes. That's where Dragon being faster could really speed things up.
2. I needs faster way to collect [structured data](/2011/snappy-charting/). **The answer is autocomplete.** I'm intending to make an autocompleter that adds diagnoses, prescribes meds, and captures my plan. I think it'll bring the snappy feeling to much of my charting. Just like I currently have snappy for order tracking and taskman with my [e-MDs macros](/2011/e-mds-macros/).

As the years go by, Dragon gets better and better. With all the work, it seems like upgrading could improve things. The problem is that the Professional Version is locked out of EHRs. Nuance says:

    This edition of Dragon does not support dictation directly into Electronic Medical Record (EMR) Systems. For EMR support, please use Dragon Medical Edition.

The Problem: Dragon Medical Edition costs  $1600 and feels like 'This is a *hospital bandaid* so it costs *$24*" So even if you don't need all the higher-end features of the Medical Edition, you're stuck.

Say Dragon Medical @ $1600, saves you 10 minutes a day (based on my current usage, that's my guess once I'm up to speed.) So ROI for me is about 9 months.

Dragon Premium costs $150. Say it's not nearly as efficient and only saves 8 minutes. Still ROI is a little over  1 month. Add in a few hours of training and setup, and we're talking 2-3 months for a significant workflow redesign.

My real question: **Is Premium even less efficient than Dragon Medical**? I'm sure they've tuned Dragon just like they've done for teenage speakers or for speakers with a Great Lakes Accent. (I'm not kidding, those are improvements in recent Dragon.) And tuning improves accuracy I'm sure. 

But Accuracy is a neverending quest. As a family doc, my dictation is much closer to regular english than it is to, say, an MRI report from a radiologist. if I was a radiologist, I wouldn't even hesitate to have Dragon Medical with all the optimal training and microphone and custom macros. But my use case is different.

I think using [practice-based evidence](/2011/practice-based-evidence/) is the key. I start with an empty vocabulary. Luckily I have about 3 years of dictations in electronic documents so I feed that into Dragon. Boom: I've got a custom dictionary of ~25K words that I've personally said with language adaptations for my style of wordiness. I don't have a report (yet) but I'll be adding words from my e-MDs visit notes, too. Those notess I won't have language adaptation since I almost never dictate the same as what our generated text would say. I'll add a list of words of every drug I've written in the past few years. I'll add a list of every diagnosis I've done. 

That will make a dramatically more customized vocabulary than I'd get with Dragon Medical out of the box. And a relatively small vocabulary so performance will be better. 

I have a small macro that turns my microphone on (and switches to Notepad to get around the limitation in Dragon Medical). Then  when I'm finished, I hit the same key again. That turns off the macro and pastes it back into the free text.

## Version 1

	Numlock::
	IfWinActive, Free Text
	{
	WinGetPos, xpos, ypos, width, height, A
	run, Notepad
	WinWaitActive, Untitled - Notepad
	WinMove, A,,%xpos%,%ypos%,%width%,%height%
	Send {NumpadAdd}
	return
	}
	IfWinActive, Untitled - Notepad
	{
	Send {NumpadAdd}
	sleep 50
	Send {Control down}
	Send a
	Send x
	Send {Control up}
	Send !F
	Send !x
	Send !n
	IfWinExist, Free Text
	{
	WinActivate, Free Text
	WinWaitActive, Free Text
	}
	Send {Control down}
	Send v
	Send {Control up}
	send !s
	}
	return


### Other Setup

Put Dragon in Tray Mode. Screen space is golden.

### Next Version: Note Integration

If we really are going to 'integrate with your EMR', we need a macro that makes it easy to dictate. I'm thinking I'll make a toolbar that covers the note navigation toolbar. It'll be hardwired to the appropriate free texts. So ROS will go to that free text. And Assessment will go to the free text after each assessments. (I'll have several assessment buttons since I often have multiple) By eliminating trying to click the tiny little free text circles (You know, ![](/files/2011/03/freetext.png)) it should be much less stressful to dictate and to hop around the note. That hopping is part of what stresses me out. I am typically going back and forth. As dictation gets better and better the going up and down the note start to take more time respectively.

I don't want to over-estimate here but I think my little note navigator part will actually make Dragon faster in e-MDs than Dragon Medical. I'm going to be using this with Dragon 11 Professional (since that's what I have) but it ought to work fine with Dragon 11 Premium  that costs [$137 on Amazon](http://www.amazon.com/Nuance-Communications-Inc-K609A-G00-11-0-NaturallySpeaking/dp/B003VNCROU/ref=sr_1_1?ie=UTF8&qid;=1301274621&sr;=8-1).


