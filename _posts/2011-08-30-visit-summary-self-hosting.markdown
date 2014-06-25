---
author: jploudre
comments: false
date: 2011-08-30 05:27:33+00:00
layout: post
slug: visit-summary-self-hosting
title: Visit Summary Self-Hosting
wordpress_id: 915
categories:
- software
tags:
- e-MDs
- simplicity
- usability
---

**Note:** *This is a post from 8/2011 -- this article won't stay up to date. If you are going to self-host, you need to pull original files off the server.*

When I first got e-MDs 7.0, one of the first things I did was look at the Visit Summary. As I went to lunch a few minutes later, I brainstormed how I could bypass the formatting and create my own theme. I originally imagined putting up this set of downloadable files. Unfortunately, my plan for formatting requires a web server. And my regular server (for unchart.com) wasn't going to work. So I figured out how to host on [Amazon's Web Services](/2011/amazon-web-services/). I've been pretty pleased with the performance. 

Here are my raw files. You can host it yourself if you think you'll have better uptime than I do. Hopefully e-MDs will make this superfluous but we'll have to see what they do in  7.3.

Here's how I organized the files on the server:

     /cda.xls
     /phone.png
     /user.png
     /signpost.png
     /medical-bag.png
     /cdastyle/cda-styles/cda.xsl
     
I'm not sure I still need to host the cda.xsl at the root but I did during development. In both xsl files you'd need to change '50.18.44.12' to whatever your server address is so the pictures show up. (The .png's are hardcoded into the xsl.) You'll probably want to change the picture at the top (ncfpleaf.png, too.) I host mine on Nginx. If these instructions are too brief for your tech guru, then you probably shouldn't host these yourself.

[![](/files/2011/01/57-download.png) Unchart Visit Summary (August 2011)](/files/2011/08/Unchart-Visit-Summary-Aug2011.zip)

-----------------------

And here's what motivated me to share: **Downtime**.

I'm not sure why the server went down today (Aug, 2011). I pretty much had to accept it being down while I saw patients. **Sorry ... priorities.** Unfortunately that made my 'uptime' lose a  '9' of reliability. Before today, I think was running at 99.9% Uptime. So far, all the previous downtime was my fault -- I upgraded the format and forgot to turn on the server afterwards. I created an upgrade policy checklist so I don't do that again. And I try not to touch the server. I'm not sure what happened today. It'll take me 10 years to get back to 99.9% uptime. :-) After I rebooted the server, I couldn't restart the webserver because I was at work. I had previously locked down the server to prevent hackers and I couldn't really get to it from work (without investing time I didn't have between patients). So good server security was the problem for quick service.

That said, this was frustrating ~400+ times -- my guess of current traffic on the server. Sorry.
