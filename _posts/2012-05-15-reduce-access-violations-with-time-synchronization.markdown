---
author: jploudre
comments: true
date: 2012-05-15 15:22:08+00:00
layout: post
slug: reduce-access-violations-with-time-synchronization
title: Reduce Access Violations with Time Synchronization
wordpress_id: 1261
categories:
- software
tags:
- e-MDs
- usability
- workaround
---

Thanks to Jeff Grabenstein, MD, of Family Doctors of Oak Ridge. He's been exploring this lately and wrote this summary.

----------------------

Jeff's Current Recommendation (Free):  [![](/files/2011/01/57-download.png) NetTime](http://timesynctool.com/)

## Daily frustration with access violations

I have been a user of e-MDs solution series since 2000.  Many years ago I learned that I needed to know as much about computer hardware as my IT specialists did.  I have seen many changes in e-MDs and it supporting hardware.  I have tried to keep my hardware at or beyond their minimum requirements.  Somewhere in the transition to their version 7.0 and greater and with the inclusion of Windows 7 my network began to notice more connection failures.  I have made all of the e-MDs suggested changes but I would continue to have between 2 to 4 connection failures on my Windows 7 client every hour.  The rest of the office is running Windows XP and they would have about 2 to 4 connection failures a day for each client.  

My IT security guru told me that one of the nice things about Windows server 2008 is that it can update its time over the internet and be sure that all of the network computers have the same time.  This was the first that I had heard about syncing all of the clocks on a domain to one central "time server".

There are limits to Windows Time Servers ([Microsoft KB article](http://support.microsoft.com/kb/939322).)

## Measuring Time Variation

Before I could replace my windows 2003 server domain controller I found a freeware network clock analysis tool [LMcheck ](http://www.greyware.com/software/domaintime/instructions/tools/lmcheck.asp)from a company called [greyware ](http://www.greyware.com)that sells a program, Domain Time II, to help automate the task of domain time keeping.  My analysis revealed that my domain had tremendous variance its computer time from one computer to the next.  

     Worst Variance:   00 000 00:00:02.192	>2 secs

I eventually found another freeware program called [NetTime](http://timesynctool.com/) that I have since installed.  I have set up one server to be my time server.  It updates the domain time from the internet every 15 minutes.  The other members of my domain then sync their clocks to this "time server" every 20 minutes.  Some people feel that using the internet to set domain times is a security risk.  There are companies that sell domain time servers that update their clocks from GPS systems or the cell phone network.  These devices cost around $3000.

Since I have implemented this time sync I have at most about 1 access violation a day on my Windows 7 client and the Windows XP clients have not had any access violations.  Yesterday I did not have a single access violation.

