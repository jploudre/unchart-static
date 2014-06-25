---
author: jploudre
comments: false
date: 2011-03-04 23:32:43+00:00
layout: post
slug: snappy-charting
title: Snappy Charting
wordpress_id: 481
categories:
- theory
tags:
- abbreviation
- efficiency
- macro
- usability
---

*Note: This article requires 20+ minutes to read the accompanying materials and videos.*

With all these Gigaherz and Gigabytes and stuff, why is charting so slow?

We all have gut awareness of speed. Snappy. Quick. Pop. ....These aren't really the words people think of when interacting with an EHR. And this isn't a computing problem (not enough CPU, RAM, Hard Drive, Network or whatever.) This in an interface problem. How do you speed up a process that produces unique products? This is like the difference between homemade chili made with homegrown beans and store-bought. We're trying to distill a unique visit between a doctor/patient into a unique written record.

This gets rapidly philosophical. The two sides of how to do this are probably "Narrative Medicine" and "Structured Data." Narrative medicine champions the uniquness and individuality. It's typified by voice dictation with all the flavor and information it contains. It's not canned or vanilla or generic. And Narrative Medicine argues that EHRs are stipping our all our humanity. Structured Data focuses on being able to leverage the tremendous data at our hands to improve care and quality. But if we're going to report data out (say, who needs a flu shot) you need to have structured data (codes like ICD/CPT/etc). Computers needs codes to do their number crunching. We all hate assigned codes but it's not going away.

The gap between narrative medicine and structured data is huge and isn't going away soon. Tech like voice recognition and natural language processing are going to help but don't count on this getting solved soon. Mapping something like 'Bob's back today to talk about his recent sugars' to 'Diabetes, Type 2, Requiring Insulin, Uncontrolled' isn't that easy.

So: Better Hardware isn't going to help. And maybe someday the EHR will know what we mean, but don't hold your breath. **The way to improve snappiness is to focus on the person.** So things like usability, user experience, interface bandwidth, typing speed are what really matters.

-----------------

### Kill off Hunt and Peck Typing

Do you know anyone who  hunts and pecks? They'll essentially never get a sense of flow or snappy work. Take a couple hours a week and start practicing. Maybe spend $20 on some Mavis Beacon software but start practicing. Typing without looking at the keyboard is a fundamental requirement of modern EHR use.

(Does any clinic actually perform typing tests as part of hiring?)

----------------

### Latency and Bandwidth

To really understand snappiness, we're going to need some vocabular. Latency and Bandwidth are networking terms. If you're trying to figure out why 'the internet is slow today' you'll need both. Tidbits probably does the best discription even though it's pretty old. As you're reading, you don't want to get mired. I'm going to be using these ideas of latency and bandwidth as it relates to usability. (Say Interface bandwidth or attention latency)

* [Bandwidth and Latency: It's the Latency, Stupid (Part 1)](http://www.tidbits.com/article/729)
* [Bandwidth and Latency: It's the Latency, Stupid (Part 2)](http://www.tidbits.com/article/723)

Go ahead. Go over to Tidbits. I'll wait for you to come back....

### Interface Bandwidth and Latency

A useful theory, [Keystroke Level Model](http://en.wikipedia.org/wiki/Keystroke-Level_Model),  goes back to the early 1980s before the first modern Mac -- the first Mac.  Home computers existed before the Mac, but the original Mac is the first computer you (now living in 2011) could sit down in front of it and be comfortable using it. Keystroke Level Model describes how fast a person can get something done on a computer. So when you're figuring out what's the fastest way to chart you need to balance clicking and typing.

If you type 50 words a minute, you're hitting 200 keys a minute. In that same minute, you might be able to point and click 30 or 40 times. So is it faster to type the paragraph or template? 

In Video, [10GUI](http://10gui.com/video/) shows a futuristic interface. The specifics may not be available now but the ideas are still enlightening.

So there's the philosophical basis for why I focus so much on abbreviations and macros. People think I'm crazy to make a macro that saves 4 or 5 clicks. But I've got low latency with my hands on the keyboard and pretty decent bandwidth. I can type without looking at the keyboard so I can even do some of this at the same time as I watch a patient's expression. Mousing has much more latency and requires me to use my attention and vision to find the buttons that I'm going to click. The clicking is much much easier to learn (click on this button) than macros. But assuming an expert user: mousing is actually more work and much slower. It still can be efficient: if a few clicks can add a whole sentence (via a template) it might be faster than typing.

The larger the number of unique items, the less well a mouse works. If you have 3000 options (the size of our Orders Template, actually), you don't want a list. Even an organized list is overwhelming. If a macro can allow it to be done via typing, it could be much faster.

