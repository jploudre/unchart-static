---
author: jploudre
comments: false
date: 2011-06-01 03:12:32+00:00
layout: post
slug: provider-panel-report
title: Provider Panel Report
wordpress_id: 758
categories:
- software
tags:
- continuity
- crystalreport
- e-MDs
- managing
- report
---

This is a basic report for provider panel size. It's based on patients that have visited the clinic (not just in the database). My clinic has been using e-MDs for 3 years  so looking at all visits has been an OK shortcut. Most experts recommend using a shorter interval for estimating panel size (12-18 months, typically.) That could be adjusted pretty easily in Crystal Reports, if it was important.

This report pays attention to exempted patients (Using 'Exempt from Reports' in Demographics) if you use that in your clinic process for transferred or discharged patients.

★ Don't miss: [Provider Panel Map](/2011/provider-panel-map/)

### Adjusting? Not worth it for me.

Obviously providers have different recall style (doctors who encourage more frequent feedback need an effectively smaller panel) and different panel makeup (male versus female providers, for example.)

One time I used a set of conversion factors to adjust for the age/sex of patients. ([See Panel Equity Article](http://primarycareforall.org/wp-content/uploads/2011/05/Panels-in-Primary-Care.pdf).) Interesting experiment -- some female providers at my clinic have 85% female patients. Some docs do OB (and see lots of pediatric patient who have a lot of visits.) But rank order of panels was essentially unchanged. This simple panel measure is good enough for our clinic.

### Panel Size is clinic-wide, too.

One of the things I learned by looking at panel size is that larger clinic dynamics matter. I could fix my availability and have a right-sized panel and still have problems. If a partner is overburdened, the patients will spill over. To really get success in managing panels, I think you have to consider  the whole clinic as much as individual providers. 

[![](/files/2011/01/57-download.png) Provider Panel Report](/files/2011/06/provider-panel.zip)

