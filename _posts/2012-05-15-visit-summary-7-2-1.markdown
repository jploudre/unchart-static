---
author: jploudre
comments: false
date: 2012-05-15 04:40:25+00:00
layout: post
slug: visit-summary-7-2-1
title: Visit Summary 7.2.1
wordpress_id: 1253
categories:
- software
tags:
- e-MDs
- meaningfuluse
- patient-centered
- simplicity
---

It's been just over a year since I was appalled at the default Visit Summary.

The original visit summary disengages a patient in her care. It sets up barriers like 3/4 of a page of junk before the actual content begins.

So that night as a proof of concept, I [cleaned up the Visit Summary](http://unchart.com/2011/visit-summary-cleanup-1-0/). I started using this for my own personal summaries by redirecting e-MDs stylesheet to my own. 

If I wanted to share this with other people, I had to set up a webserver. So a month later I set up my [Unchart Visit Summary](http://unchart.com/unchart-visit-summary/). Initially I required payments to get the installation instructions. Mostly because I didn't want to start doing a bunch of tech support. Much to my surprise, some people actually paid me. After a few months, I had gotten enough help to pay my server costs that I made donation optional.

After one of my brief downtimes, I also set up directions for [self-hosting the summary](http://unchart.com/2011/visit-summary-self-hosting/) for people who didn't want to rely on a server they didn't control. Over the last year I got 99% uptime. Which is kinda lousy but I learned a lot. I've now got a 15 step server upgrade process. And I've accumulated several testing procedures to limit errors. I think I may get 99.95% this year.

So now that I've finished my adjustments for 7.2.1 (and e-MDs has made a redesign of their initial summary), where are we at?

### Major improvements from e-MDs

The best improvements from e-MDs center on making the information more approachable.

* Reordered problems so names came before ICD codes
* Cleaned up med list info (No RxNorm Codes, etc)
* Reduced visual complexity by turning tables into lists.

### Main Ongoing problems from e-MDs

* Legibility (10 point san-serif font)
* They use background colors for bars but these don't print right (instead get boxes).

### Main improvements from Unchart Summary

* Headline and text fonts
* Larger 12 point font size to increase readability
* More specific use of white space to direct attention. 
* Cleaner appearance. 
* Removal of HPI (now an option from e-MDs) allows more visit summaries to be available at the visit (with an incomplete note.)

![](http://unchart.com/wp-content/uploads/2012/05/Screen-Shot-2012-05-14-at-9.33.56-PM.png)
