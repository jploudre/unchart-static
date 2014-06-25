---
author: jploudre
comments: false
date: 2012-06-08 17:59:57+00:00
layout: post
slug: ideal-panel-size-report
title: Ideal Panel Size Report
wordpress_id: 1281
categories:
- software
tags:
- crystalreport
- e-MDs
- managing
- patient-centered
- report
---

A few years ago the AAFP had an article, [How Many Patients Can One Doctor Manage?](http://www.aafp.org/fpm/2007/0400/p44.html). This report can be used for dicussions about relative panels in a practice. Which doctors have availability that matches up with their assigned panels? Who is over-paneled? Who is under-paneled?

This crystal report for e-MDs has 4 different tables that you can use to determine the answers to those questions.

The first table has the number of distinct patients assigned to a doctor with visits/invoices in the last 2 years. (People use different timeframes from 1-3 years typically when defining active patients.) *So, for our practice certain types of visits, like prenatal visits, don't show up here.*

The second table shows the number of visit/invoices that the patients had in the past 2 years (regardless of continuity.)

The third table shows the number of visits/invoices that the provider gave in the past 2 years (regardless of continuity.)

And the last table shows the number of continuity visit/invoices for the providers and patients.

[![](/files/2011/01/57-download.png) Ideal Panel Size Report](/files/2012/06/ideal-panel-size-data.rpt_.zip)

The real question for a group: **Could you use this kind of data to make decisions about how to manage panel sizes?**

---------------

Curious what counts as a visit/invoice? No list is perfect. But here's the CPTs embedded in the report:


     '99245','99201', '99202', '99203', '99204','99205',
     '99381','99382','99383','99384','99385','99386','99387'
     ''99211','99212','99213','99214','99215','99391',
     '99392','99393','99394','99395','99396','99397'
     '99253','99254','99255','99231','99232','99233','57410',
     '56605', '56606', '56620', '56625', '56630', '58120', '58558',
     '57065','57500','57505', '57520', '57522', '57155','56630',
     '56631', '56632', '56633', '56634', '56637', '58150','58200', 
     '58720','58943', '58951','58953','58954','58956','44005',
     '50715','44955','57531','58210'
			
