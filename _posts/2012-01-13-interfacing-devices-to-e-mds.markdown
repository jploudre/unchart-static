---
author: jploudre
comments: false
date: 2012-01-13 21:29:04+00:00
layout: post
slug: interfacing-devices-to-e-mds
title: Interfacing Devices to e-MDs
wordpress_id: 1091
categories:
- software
tags:
- e-MDs
- efficiency
- proofofconcept
- technology
- workaround
---

John Crankshaw mentioned a process for interfacing devices to e-MDs (without having to buy the more expensive models that are supported.) 

[![](http://unchart.com/wp-content/uploads/2011/01/57-download.png)Printable Word Document](http://unchart.com/wp-content/uploads/2012/01/ZanimageDocmanBatchscreenshots.docx.zip)

Take it away Dr. Crankshaw....

-------------

### Using the Docman Batch Import Utility as an Interface

Our office uses the Docman Batch Import Utility along with a tiff converter, zan image printer, to upload into e-mds many different documents.   We auto import results directly into a patient’s chart from our Midmark EKG, Holter, PFT computer.  We also auto import directly into a patient chart lab results from our Labdaq system from our in house Lab.  I also use it to import documents from the Hospital online Portal and our state immunization registry.  These documents appear in e-mds as tiff documents just like any other scanned document.  The following is an example of how we have set up our system to auto import documents from the Midmark computer.
Since the Midmark system allows us to add the e-mds ID to the demographics, we are then capable of importing the results directly into the patients chart.  The zan image printer, during tiff conversion, is able to scan the document for the e-mds ID and include it in the file name, which then allows the Docman Batch Import Utility to import the document directly into the patient’s chart and notify a user the results are ready.  
The first step is setting up the Docman Batch Import Utility if you haven't set it up yet.  It should be installed on just one computer.  The utility is on the latest e-mds solution series disc if you haven’t installed it.  When you install from the e-mds disc, click custom and check it off.   I would recommend looking at the instructions for the Docman Batch Import Utility on the last disc you have from e-mds or download the instructions from the e-mds support center.  It will walk you through the installation steps.   The Docman Utility gets installed as a service on your computer.  The utility needs to have constant access to the shared folders it is monitoring.  If the shared folders are on a different computer and that computer is turned off, then the utility will not work when that other computer is restarted.   The service will need to be restarted.    I recommend that the computers that have the shared folders be constantly on.   Here is a screenshot of the Docman Utility Service:

[![](http://unchart.com/wp-content/uploads/2012/01/docman-utility-300x224.png)](http://unchart.com/wp-content/uploads/2012/01/docman-utility.png)

After installing the Docman Utility, you will need to set up shared folders on the computer you will be downloading results.    The following are screenshots from our Midmark computer of the folder setup: 

[![](http://unchart.com/wp-content/uploads/2012/01/midmark-import-150x150.png)](http://unchart.com/wp-content/uploads/2012/01/midmark-import.png)[![](http://unchart.com/wp-content/uploads/2012/01/midmark2-150x150.png)](http://unchart.com/wp-content/uploads/2012/01/midmark2.png)

Finally, you will have to change the settings in the Docman Utility.  The following are my settings for the Midmark import:

1.  Default Docman Category...:  Cardiovascular (you choose which ever you like though)
2.  Parsing Options:  Second for Patient Account Number, Third for Document Description, and the rest I left Not present.
3.  Delimiter _ (underscore)
4.  File Extension * (asterisks)
5. Time to wait - 90 seconds
6.  Auto Tasking -  Check Send Taskman message -  then choose who you want to receive the message when imported and who should get a message if it didn't work right.   (exception).

[![](http://unchart.com/wp-content/uploads/2012/01/docman-settings-150x150.png)](http://unchart.com/wp-content/uploads/2012/01/docman-settings.png)

The next step is installing and setting up the Zan Image Printer on the computer you will download the information to.  For us, we installed it on the same computer that has the Midmark software.  The Zan Image Printer is third party software that has a nominal cost. http://www.zan1011.com/ 
 (Disclosure: I have no relation financially with the makers of Zan Image printer).
 
When I install it, I install a color version and bw (black and white version).  The black and white version is what I use.  The zan image printer installs just like any other printer.  Go to the Printers and Faxes for window XP or Devices and Printers for Win7.   Right click and click printing preferences.
I'll go through each tab in the printing preferences with screen shots for each. (See the download for all the images.)

1. Layout - No changes
2. ￼Paper/Quality - Paper Source - Automatically Select;   Color - Black & White	￼
3. Save – Folder - click browse and browse to the shared folder you created;  File Name:  Click Macro and pick at the bottom Regex Document Name.  Then make sure the File Name looks like this:   Document_[%RegexDocName]_EKG-Holter-Spirometry   (the EKG-Holter-Spirometry part you can change to any name you want.  This is what the documents name will be in docman when imported) When File exists: Show warning dialog. Before Printing... - No Dialogs

---------------

[![](http://unchart.com/wp-content/uploads/2011/01/57-download.png) Download the printable Word Document with all the screenshots](http://unchart.com/wp-content/uploads/2012/01/ZanimageDocmanBatchscreenshots.docx)**

----------------
![](http://unchart.com/wp-content/uploads/2011/03/joker.jpg.jpg)

This was shared by John Crankshaw, MD
