---
author: jploudre
comments: false
date: 2011-09-02 05:23:43+00:00
layout: post
slug: unfocus-the-mouseless-plan
title: 'Unfocus: The mouseless plan'
wordpress_id: 921
categories:
- software
tags:
- e-MDs
- efficiency
- macro
- proofofconcept
- usability
---

It's difficult to get a visit summary done in real-time without tradeoffs. (Sarcasm alert.) I'm awesome at tech can totally get them done. Why can't everyone just click quickly? Seriously, though, I end up having one of these options:

* Ignore the patient and  what they are saying while I click away
* Dead Airspace while the patient waits for me to click
* Leave the room for a couple minutes to click without the patient right there.... except then
* Ignore my nurse or get distracted by some other task.

In e-MDs, the automation for filling out a template is the preclick. Call me a luddite but that level of 'macro' doesn't work for plans. If you preclick a whole plan you risk integrity -- documenting something you didn't do. And there's enough variablity of the same few things that you can't really macro the group. Am I going to have a preclick  for 'Call 1 week, OTC Meds, No Labs' another for 'Call 1 week, OTC Meds, CBC' another for 'Call 1 week, OTC Meds, Rx Med, No Labs' and so on?

The plan is [structured data](http://unchart.com/2011/snappy-charting/) and ought to be done with a template instead of narrative text. Even though I might dictate the plan faster, it's right to use the template. Using the template, for example, could let me set up a system to have my nurse check back on a patient who is trying a prescription.  We may not exploit the precision of structured plan data now but I still think templates are the right way to go.

What I need, is a way to get the plan together without needing to focus attention and click. Reminds me of a wonderful usability technique: [The $5 Guerrilla User Test](http://blog.bumblebeelabs.com/the-5-guerrilla-user-test/). Basically, the premise is that usability for distracted users can be mimicked by testing on people buzzed on alcohol. The reality of clinic is that the busyness is distracting. It's not like I have free/unhurried time to document the plan. I've got a patient waiting for the visit summary, another waiting for me to start the visit, I'm personally waiting for the summary to come out of the printer and my nurse is waiting to see if she can snatch an answer to something she's working on.

# Unfocus: Action without Doing

Here's my answer:  Wei wu  wei. It's a Taoist principle. Could be interpreted as Action through inaction. Or  Creative Inaction. Or my favorit: Action without Doing. By having the computer read my mind with a few keystrokes, I can get the plan without focusing on the screen. In the video here, I've typed this to create my plan:

     F5 `c1w `med flonase `dmed `dotc `drexam
     
Which the computer translates to

     Open first plan  
     Call in 1 week if not improving  
     New Medication (Flonase)
     Discussed medication and side effects
     Discussed OTC meds
     Discussed the reassuring exam.
     


[UnFocus in e-MDs](http://vimeo.com/28491927) from [Jonathan Ploudre](http://vimeo.com/user8098140) on [Vimeo](http://vimeo.com).



You probably noticed all the ` marks. That's my signal to the computer to listen up, I'm going to type something and I want you to read my mind. I've got about 170 commands covering common labs, all the options for medications or followup. They all roll off my fingers since they are mnemonics that I made. I could literally do this plan with my eyes closed. 

This dramatically uncompresses the 20-30 most stressful minutes in a workday. It's not much faster but it allows me to document and maintain eye contact with my patient. Or document on multiple plans without feeling overwhelmed. 

And it's a foundation for errorproofing. Soon when I document a medication, it'll automatically pop me into the the prescribing window with the med searched for and ready to select. (Eliminating double entry.) 
