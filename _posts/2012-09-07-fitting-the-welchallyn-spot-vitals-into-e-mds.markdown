---
author: jploudre
comments: false
date: 2012-09-07 17:14:38+00:00
layout: post
slug: fitting-the-welchallyn-spot-vitals-into-e-mds
title: Fitting the WelchAllyn Spot Vitals into e-MDs
wordpress_id: 1312
categories:
- hardware
- software
tags:
- e-MDs
- efficiency
- managing
- SpotVitals
- usability
- workaround
---

![](/files/2011/08/450x0-E1-2-150x150.jpg) After I attested for 2011 Meaningful Use, my group decided to have the doc decide on some of the 're-investments' in our practice. The second thing I got was the WelchAllyn SpotVitals Lxi. (Bigger monitors for reception was first.) I had been interested in this for at least a couple years. A while back, I posted a [video on using the SpotVitals](http://unchart.com/2012/welchallyn-spotvitals-lxi/).

Automated vitals addresses a few different issues for my practice:

* Using an interface eliminates typo errors (which can cause embarrassing mistakes graphing, say, weight.)
* By checking blood pressure on the way up, the SpotVitals is faster.
* By speeding up vitals it can allow the nurse/MA to focus more on the person
* Clinical Research shows that labile blood pressure readings are improved with automatic vitals over manual vitals.
* Reduces inter-staff variability in blood pressures.
* By having a central station, it's much better stocked (every single cuff size is handy, no having to walk for a thigh cuff.)

So, sweet, right?

Unfortunately, reality hasn't quite worked that way. The SpotVitals is expensive so you don't just order one per nurse. We got our first one (without O2 Sat) for about $1700. It's an extra $1300 to add O2 Sat. WelchAllyn's milking this, if you ask me. The price is off by an order of magnitude. This is the [same problem with Welch-Allyn's Ambulatory Blood Pressure Monitor.](http://unchart.com/2011/ambulatory-blood-pressure-monitor-wheres-innovation/)

e-MDs has an interface -- that's why we bought this specific mdoel. *It's supported.* But it's not really. The interface is a hack outside of e-MDs.It adds enough friction to eliminate the usefulness. The process is: Open Interface, Find Pt, Get Vitals, Close Interface, Open e-MDs, Find Pt, Drop in vitals. If the interface was within e-MDs you could cut the number of steps in half. And although documentation says the interface also works with compatible scales, it's been broken for a few years according several users. (Thanks Keith for saving me money on a wasted scale!)

Since the machine is expensive, we've been re-working clinical processes. Lately we've been trying doing vitals out in the waiting room. There are some communication issues between staff. On our next pilot, we're going to add a few 'rooms' to our clinic dashboard. There will be 'Vitals-Room' and 'Vitals Done' so clinical staff can tell where a pt is in the process (and if there's a backup, they can route around it.) My goal has been to help my staff decide what they want (not tell them.) So we're still trying different things out.

----------------------
![](/files/2012/09/vitalsbackground-300x185.png)

Since the interface doesn't work for efficient workflow, I'm building a new 'pseudo-interface'. This will pop up from within a patient's chart in e-MDs. I'm working with my staff to figure out the best place to put this. I'm trying a couple different things to make this work. First, much larger font-size so they can see typos better. The left side of this maps to where the vitals are on the machine. (Faster for staff, less cognitive-load so less error prone.) Tabbing through fields works in the order that they work (Again, faster). The results will be put into e-MDs where there's full details -- for example, which arm for the blood pressure. So we simplify input for reliability. 

If you'd like to help test this,  [you can drop me an e-mail](http://unchart.com/about/).



