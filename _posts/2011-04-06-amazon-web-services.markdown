---
author: jploudre
comments: false
date: 2011-04-06 05:48:45+00:00
layout: post
slug: amazon-web-services
title: Amazon Web Services
wordpress_id: 638
categories:
- software
tags:
- server
---

One of the first things I did when I got to start testing e-MDs 7.0 was look at the Visit Summary. I was horrified and delighted. Horrified at the layout, design and usability for patients. Delighted that Meaningful Use requires standards -- I could fix it.

My process of rewriting required setting up a server to host the formatting. I decided to go with Amazon Web Services. Mostly based on reputation -- Amazon.com isn't going out of business any time soon. And their expertise in running one of the biggest sites on the Net makes them very capable and managing servers.

I pretty much went with basic defaults: A Micro Instance, the Amazon Linux Image, Nginx for webserving. If you pre-purchase this server it's pretty inexpensive. ~$50 for a year or ~$80 for 3 years. And Amazon guarantees 99.95% Uptime. That's about 1 hour downtime during my work year. Given that they do planned maintenance in the middle of the night, I suspect there will be effectively 99.99% uptime. Now that I have it up I'm not intending to touch it -- no administrator errors for me!

Surprisingly, this inexpensive virtual server outperforms e-MD's official server. I tested with apache benchmark, 100 requests, 5 Concurrent Users.

||My Amazon.com Server|e-MDs cdastyle server|
|----|----|---|
|Requests/second|**8.3**|4.4|
|Longest Request|**661ms**|4730ms|

[Full Server Testing Details (4.5.2011)](/files/2011/04/server-testing-4.5.2011.txt)

