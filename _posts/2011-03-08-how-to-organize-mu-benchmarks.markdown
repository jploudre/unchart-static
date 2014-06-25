---
author: jploudre
comments: false
date: 2011-03-08 05:00:35+00:00
layout: post
slug: how-to-organize-mu-benchmarks
title: How to organize MU Benchmarks.
wordpress_id: 487
categories:
- software
tags:
- crystalreport
- e-MDs
- meaningfuluse
---

One of the main troubles with Meaningful Use (MU) is that there are so many benchmarks. It's great to have them all (now we have an agreed upon target) but keeping track is a pain. In my practice we've got a dozen providers. As it stands now, we'd need to run report after report after report to see where we are. And if we're not careful, we'd waste hundreds of pages of paper in the process. Just entering all the parameters to run the reports will take real time. 

*Ahh, a dashboard*. People think data visualization is about making everything simplify down to just a few key speedometers. Sure, as we get close to compliance, it may be a single "Go, No Go" type metric of do we meet all the intended benchmarks.

But as I mentioned in my [Data Driven Practice](/2011/data-driven-practice/) at the User Conference, visualization is about making data usable to people. Not just the geeks. Making this visual is really important. Most [decent visualizations](http://mygengo.com/talk/blog/why-your-startup-needs-a-visual-dashboard/) will engender much more attention than any table of numbers. Couldn't it just be a single page of paper?

Different organizations will have different ways of organizing. This could be a starting point about how to organize subsets of benchmarks. I'm using my short titles for benchmarks based on my Meaningful Use Map:

[![](/files/2011/02/MU-measures-300x224.png)](/files/2011/02/MU-measures.png)

### Core versus Optional (and what optional benchmarks are you aiming for?)
### By **Eligible Provider** (all the benchmarks on 1 page)
### Audience?

* **Front Office:** Demographics, Patient List, Patient Reminders, Portal (signup).
* **Clinical Staff:** Vitals, Allergy List, Medication List, Smoking Status, Medicine Reconciiation.
* **Admin/Records:** Drug Interactions (turned on), transmit CMS, Electronic Copy, Exchange Clinical Info, Security Audit, RxHub (turned on), Lab Interface, Immunization Registry, Syndromic Surveillance.
* **Docs:** Problem List, Electronic Rx, CPOE, Clinical Decision Support, Clinical Summary, Patient Education, Summary of Care.
### Now vs. Later (What could you already report with older EHR Software?)

* **Now:** Demographics, Vitals, Problem List, Allergy List, Med List, Electronic Rx, CPOE, Drug Interactions, Clinical Decision Support, RxHub, Lab Interface, Portal,
* **Needs 7.0:** Smoking Status, Transmit CMS, Clinical Summary, Electronic Copy, Exchange Clinical Info, Security Audit, Patient List, Patient Reminders, Patient Education, Medicine Reconciliation, Summary of Care, Immunization Registry, Syndromic Surveillance.
### Target Goal

* **Improve Care:** Demographics, Vitals, Problem List, Allergy List, Med List, Smoking Status, Electronic Rx, CPOE, Drug Interactions, Clinical Decision Support, Transmit CMS, RxHub, Lab Interface, Patient List, Patient Reminders.
* **Engage Patients:** Clinical Summary, Electronic Copy, Portal, Patient Education
* **Coordinate Care:** Exchange Clinical Info, Medicine Reconciliation, Summary of Care.
* **Security/Privacy:** Security Audit.
* **Public Health:** Immunization Registry, Syndromic Surveillance.
### Easy vs Hard Benchmarks
    
## Dashboards, Again

What I imagine is doing each of those bolded targets above on a single page. My group has about a dozen providers and any of those reports ought to be doable without requiring a Microfiche to read the results. Given the 90 day reporting period for 2011, these should default to the last 90 days. And as I've said before: the right number of parameters is .... zero. It should be click, go make a cuppa, come back to a fancy printed report that you post on the wall for all to see.

----------
e-MDs has stated they have a 'dashboard' in development. I don't know which of these approaches it will take but hopefully we'll see in the next few months.
