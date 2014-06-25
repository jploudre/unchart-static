---
author: jploudre
comments: false
date: 2012-03-10 17:56:53+00:00
layout: post
slug: medicare-e-rx-report
title: Medicare e-Rx Report
wordpress_id: 1189
categories:
- business
- software
tags:
- e-MDs
- efficiency
- managing
- mistakeproof
- simplicity
---

The Medicare e-Rx code drove my practice crazy last year. We e-prescribe all the time and many of us successfully attested for Meaningful Use. But the e-prescribing rule doesn't allow for tracking that way. Instead it requires *a bonus g-code* be submitted.

Please, Medicare, stop the madness!

Sara Evans rightly recognized this as a reporting problem. My clinic did not. So near the end of the year, we had to post orange signs to remind all the docs at our clinic to remember to do the extra click on Medicare patients if we did an electronic prescription. This [deskills](http://unchart.com/2011/deskilling/) us and distracts us from doctoring. In our case where we can prove we e-prescribe, there's literally no benefit to offset deskilling.

Sara's report allows the code to be added by the biller when posting to medicare. Fewer people doing the code makes it less error prone than what my clinic did last year. I took her report (a more complete listing of all prescriptions, method of sending, etc) and simplified it. I think my changes work (it results the same as when I hard-coded our doctors into Sara's report.) **But you need to validate that this report is accurate for your practice.** 

This reports people seen in the last 5 days, who have Medicare, and who had an e-prescription done in the past 5 days. In our practice docs don't do e-prescribing outside of visits (Nurses handle refills) so for us, this is a valid shortcut for e-prescription with a visit.

[![](/files/2011/01/57-download.png) Medicare Prescription Check](/files/2012/03/Medicare-Prescription-Check.zip)


---------------

### Report by Sara Evans

For the past five years, Sara has managed her husband's practice, Evans Dermatology Partners.  Prior to that, she was a management consultant with McKinsey & Co. in Dallas and London.  At McKinsey, her work focused on streamlining clients' retail store operations.  Her undergraduate degree is in Russian from Wesleyan University and she has an MBA from Duke University.  She and her husband Colby live in Austin, TX and have three children.

![](/files/2011/03/sara_evans.jpg.jpg)


