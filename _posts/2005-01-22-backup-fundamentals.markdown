---
author: jploudre
comments: true
date: 2005-01-22 16:30:59+00:00
layout: post
slug: backup-fundamentals
title: Backup Fundamentals
wordpress_id: 250
categories:
- hardware
tags:
- computer
- mistakeproof
- server
---

Having an electronic medical chart requires a well coordinated backup strategy. It's not all that complex -- despite what computer professionals will tell you. The basics of backup have not changed in the last decade and they are not likely to change in the next. What changes are the details like what type of media (floppies became Zip Disks became Writeable CDs became Writeable DVDs.) So Here are the fundamentals:

* *Automatic:* Backups are too important to require a person to remember. They need to happen without intervention.
* *Off-Site:* If you building burns down, having a backup is no good. Or if someone attempts identity theft, they might steal all your disks along with your server. Separating the backups physically increases reliability.
* *Multiple:* You are trying to avoid a single point of failure. That's the point of backup. It doesn't do you any good if your hard drive crashes and when you try to restore from backup your only copy doesn't work. Think of this: Once I had a crash that damaged a paper I was writing. I tried to restore from my floppy (1993!) but the floppy was bad. But I had thought ahead. So I got my backup backup floppy! It was bad too. That's when I realized that the floppy drive itself was bad. And it had just damaged both copies of my backup. 
* *Verified:* The point is being able to restore the data. That needs to be tested. Verification can be easily built-in and it can double how long a backup takes.
* *Fresh:* Even if you multiple backups, you should rotate in new backups and save old ones somewhere. You don't want to have three very old backups only to find out that you had a bad batch of media at the beginning that is affecting them all.
* *Frequent:* How much data can you lose and still be OK? If your practice lost a weeks worth of charts would that be fine? I'd guess not. In a medical office setting the record should probably be backed up every day.

Although it's a bit old, Adam Engst wrote a 3 part series:

* [Part 1](http://db.tidbits.com/getbits.acgi?tbart=04917)
* [Part 2](http://db.tidbits.com/getbits.acgi?tbart=04924)
* [Part 3](http://db.tidbits.com/getbits.acgi?tbart=04945) 

in 1998 that discusses backup. Again, details have changed but the fundamentals are sound.
