---
author: jploudre
comments: false
date: 2012-01-05 09:44:17+00:00
layout: post
slug: usability-of-the-washington-state-prescription-monitoring-program
title: 'Usability of the Washington State Prescription Monitoring Program '
wordpress_id: 1023
categories:
- Clinical
- theory
tags:
- readability
- simplicity
- usability
---

The idea of the prescription monitoring program (PMP) **rocks**. Given that multiple controlled substances are potentially lethal, a prescriber or pharmacist should be able to verify other prescriptions. Transparency improves care.

But it's implemented with unnecessary friction. This is going to reduce how many busy docs or pharmacists are willing to go through the hassle. The more complicated and time-consuming it is, the less it's worth.

## Getting set up with the PMP

Setup on a computer might only take a few minutes so I don't want to be overly critical. Still, the virtual multi-factor security is 'Security Theater'. [Real Multifactor Security](http://en.wikipedia.org/wiki/Multi-factor_authentication) is real. Combine a Username/Password with retinal scanner and you've got a little bit of a roadblock. (In the movies, it's sometimes gross if they bypass the retinal scanner.) Or: having a physical dongle with password.  But this isn't real multifactor security -- it's just a more extended password setup with cookies and a bookmark. The obvious flaw: if my email account were compromised, anyone could set up another virtual token -- no hacking or eyeball removal required.

My suggestion: Drop the virtual 2 factor security altogether. It doesn't really improve security. All behavior on the site is being logged. They plan to audit for aberrant searching behavior. If they follow through on that, it's enough.

## Usability Issue: Repeated Usage/Privacy Warnings

So, if you get a warning box every time you do a search, do you really read it? You might the first time, right? I could see where there should be a usage and privacy policy. Curent design is to have it interrupt you every time you log in. It's not much of a welcome:

![](/files/2012/01/Screen-Shot-2012-01-04-at-11.43.40-PM-300x236.png)

I doubt that 5% of users will actually read it after the first time. (Taunt for PMP Designers: Use your server logs/analytics to disprove me.) This looks like it was designed by a lawyer with no consideration for whether it would do anything but slow providers/pharmacists down. Um, it might have been.

Readability matters. [Alan Siegel's 5 minute Ted talk](http://blog.ted.com/2010/03/24/lets_simplify_l/) is the most damning critique of this type of information pollution. So, let's run an analysis:

* Gunning-Fog (approximate year of formal education needed): 17
* Word Count: 277
* Average Words per sentence: 23

So that's about a minute of highly concentrated attention to truly read it.

I think my version is essentially identical

> ###Practitioner/Pharmacist Statement
> 
> * I'm licensed prescriber (or designee) or dispenser.
> * I'll use this only for medical/pharmaceutical care.
> * Before I give a patient a copy, I'll be sure of identity.
> * I realize other searching/revealing of private information is illegal and could result in disciplinary action or lawsuit. This info should be protected like other Protected Health Info (PHI). 
> * I'll safeguard my password. If there are issues with safeguarding, I'll let the Department of Health know immediately.
> * I'm being watched/audited.
> 
> I agree

Just a quick rewrite but:

* Gunning-Fog from 17 to 12
* Word Count: 277 to 79
* Average Words per sentence: 23 to 9

My suggestion: Drop the required click through. And if you dramatically simplify like I'm showing above, you might actually encourage real people read it. 

## Usability Issue: Make Search Form Easier

If you move your eyes through the search form, you have a jumble of needing to carefully check everything. 

[![](/files/2012/01/Screen-Shot-2012-01-05-at-1.00.10-AM-300x247.png)](/files/2012/01/Screen-Shot-2012-01-05-at-1.00.10-AM.png)

Some of the available options, seem to be missing the whole point of a **statewide prescription monitoring program**. Why give an option to search by county? That's close to never useful. If location really mattered they would do 'within 10/25/50/100 miles'. (The DEA knows my address already without me typing it in.) 

Something like this would be better:

![](/files/2012/01/PMP-Search-Revised.png)

Honestly you could simplify to just Patient Name/DOB (since Dispense dates appear to autofill, anyhow). Just give advanced options for all those providers who only care about your zip code or county. (Why would they want to know if you go across town? Oh, wait, that's the whole point.)

![](/files/2012/01/Screen-Shot-2012-01-05-at-1.24.52-AM.png)

## Bonus Issue: Design from 1998

This is where I get crotchety. The use of tables for layout and embedded font and color formatting is something that hasn't been best practice since, um, the 1990s. There's a reason that this site has a Netscape Navigator 4 vibe: the underlying code is designed as if we're partying like it's 1999.

So I sound like a snob. But practice as a doctor is filled with unending demands for attention. Reducing friction with a modern/simpler design means I'm much more likely to use this. It's not about making it 'shiny'. It's about improving care. Usability really matters.

