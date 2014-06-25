---
author: jploudre
comments: true
date: 2011-01-29 17:50:59+00:00
layout: post
slug: prevention-checklist
title: Prevention Checklist
wordpress_id: 286
categories:
- software
tags:
- e-MDs
- efficiency
- macro
- mistakeproof
- proofofconcept
---

Here's my checklist maker for preventative recommendations in e-MDs. It uses a Word Form, pulls the patients age/sex from the form, and then creates an individualized checklist. So 22yo male will get different recommendations than a 64yo female.

Consider this a proof-of-concept as of 5/5/2010. I'm still refining it for my use and hope to eventually parse through the patient's problem list for secondary prevention recommendations. But it's working for my use.

[![](/files/2011/01/45-movie-1.png) See it in action](http://www.youtube.com/watch?v=TiiYyGDDSJg)



* **Known Issues:** On our setup, there's variable server speed. Usually the first time of the day it crashes. It seems to depend on how word forms are cached. Works reliably for the rest of the day. Unfortunately I'm not debugging our server performance so consider this proof of concept only. I still use it myself. I'll probably remove the word-form .
* **Tested on:** e-MDs 6.32

