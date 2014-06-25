---
author: jploudre
comments: false
date: 2011-07-01 14:59:24+00:00
layout: post
slug: print-to-file-to-work-around-inability-to-export
title: Print to file to work around inability to export
wordpress_id: 816
categories:
- software
tags:
- workaround
---

I'm a lover of 'postprocessing' in excel. If I can just get the data, I can do my own analysis, thank you. (Again, I'm going to plug my '[Data Driven Practice](http://unchart.com/2011/data-driven-practice/).' Amazing what you can do with pivot tables and autofilter!) Sometimes e-MDs is set up to let you download/export data. Any crystal report, for instance, can be saved as a file to process in Excel. 

But data is not always exportable.
 
Consider this problem, brought up on [supportcenter recently](https://supportcenter.e-mds.com/ics/forum/Client/Common/ContentView.aspx?contentID=106028). How do I make sure that followup notes get faxed back to the primary care provider. You can get faxing/sign off data from the treasure chest of Chart Audit. But Chart Audit doesn't allow exporting, just printing. So do I have to print out 30 pages and *manually scan through with a highlighter*? (Cue Next Line: That's what computers are supposed to do....)

### Printing to file

One of the things I love about Mac OS X is that printing to file (pdf) is baked in. Whatever mac you use, whatever program you're in. Hit print, choose 'Print to PDF' and now you've got an electronic copy. Windows can also print to PDF with free software but since post-processing in Excel is the goal, that's not the way to go here.

The trick is to create generic/text only printer. 

![](/files/2011/07/Generic_Text_Only_Icon.png)

For example, Windows XP has trouble exporting device manager info. So they recommend [installing a generic/text only driver and printing to that to create a file.](http://support.microsoft.com/kb/127156). If you follow the instructions there, you'll be able to do the same with Chart Audit. But this is the  key step:

[![](/files/2011/07/Generic-Text-Only-Driver-Selection.png)](/files/2011/07/Generic-Text-Only-Driver-Selection.png)

In e-MDs you can control printing options in Chart. But some things will just go to your default printer in Windows. So to print to file, you may need to first set your default printer to the generic/text only, then do the printing, then set it back to your default.

The text file that comes out (if it was a table of data) can usually be pretty easily processed in Excel at that point.
