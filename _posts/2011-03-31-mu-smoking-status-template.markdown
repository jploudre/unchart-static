---
author: jploudre
comments: false
date: 2011-03-31 22:03:05+00:00
layout: post
slug: mu-smoking-status-template
title: MU Smoking Status Template
wordpress_id: 585
categories:
- software
tags:
- e-MDs
- meaningfuluse
- mistakeproof
- template
---

I actually changed the orange starred part of the template so I can document both for MU and PQRI (tobacco assessment clinical )quality measure. So I only have to document the status once and then if I prescribe a smoking cessation medication or counsel a patient (and document in the plan section) I get credit for both.

The tobacco assessment and counseling measure that is part of the MU Clinical Quality Measure rule isn't tracked by the MU codes in the orange star tobacco template. That report uses the PQRI codes as dictated by CMS. e-mds doesn't have those codes as part of the tobacco template (only the MU codes).

Here are the changes I made

1. I added a child to "Never Smoked" that is a force answer called "Check for quality measure", which is also a default as checked. It doesn't drop any language into the health summary but does have the PQRI code for nonsmoker attached as an extended attribute. The MU code is still part of the "Never Smoked" click.
2. Under Past Smoker, I made the Cigarette or Cigar childs forced answers and added the PQRI extended attribute for past smoker to each of those choices. The MU code extended attribute is logged when you clikc past smoker which wasn't changed.
3. Under Current smoker - selecting "Current smoker" will log the PQRI code for current smoker and the MU code is with the "Everyday smoker" or "Intermittent smoker"

These PQRI codes will satisfy the first part of the Tobacco Use and Intervention report for Core requirement #11
the second part of the report is actual intervention - that gets satisfied if you prescribe a smoking cessation medication or you document counseling of smoking cessation in a plan template under "Smoking Status" which is in about every plan template.

[![](http://unchart.com/wp-content/uploads/2011/01/57-download.png) Tobacco_Alcohol_Supplements](http://unchart.com/wp-content/uploads/2011/03/Tobacco_Alcohol_Supplements.zip)

-------------------------

![](http://unchart.com/wp-content/uploads/2011/03/joker.jpg.jpg)

This was shared by John Crankshaw, MD
