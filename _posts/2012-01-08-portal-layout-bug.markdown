---
author: jploudre
comments: false
date: 2012-01-08 16:48:06+00:00
layout: post
slug: portal-layout-bug
title: Portal Layout Bug
wordpress_id: 1036
categories:
- software
tags:
- bug
- e-MDs
- proofofconcept
---

![](http://unchart.com/wp-content/uploads/2012/01/Screen-Shot-2012-01-25-at-7.46.18-PM.png)


**Update:** *This appears to be fixed as of today.  Interestingly enough the new formatting doesn't redesign the site but it makes exactly the change that I mention below. This makes it much more usable for patients.* -- Jonathan Ploudre, 1/25/2012


[![](http://unchart.com/wp-content/uploads/2012/01/portalscreenshot-300x190.png)](http://unchart.com/wp-content/uploads/2012/01/portalscreenshot.png)

## Why does portal look like that?

Let's do some ancient history. More than 10 years ago, *Internet Explorer 5.0* (yes, 5.0) had a bug in how it rendered layout. This is called the IE Box Model Bug. It was fixed in IE 6.0. But for backwards compatibility IE usually replicates the buggy behavior of IE 5. (So do newer version of IE, this is called 'Quirks mode') Firefox on Windows decided to replicate the bug for compatibility with IE, too. 

When portal was written, I assume they didn't even test it on other browsers besides IE. It would have been easy to fix (see below) but they weren't looking for it. To be fair, 10 years ago a lot of developers did that. And I don't know exactly when portal was developed but it was a while ago and doesn't seem to have active development.

But over the last 10 years, more and more browsers are not IE/Firefox on Windows. There are more Macs now. Google Chrome is a popular Browser. iPhone, iPad, and Android Phones. The new Kindle Fire. They all do standards-based layout so the Portal Layout Bug shows up on lots of devices. 

A year ago when I was pointing out the bug to Tech Support, their advice was that I *tell all my patients to use IE on Windows*. <del>Um, Seriously?</del>

Lest it sound like I'm a biased Mac user (which, I am), [Read about the IE Box Model Bug on Wikipedia](http://en.wikipedia.org/wiki/Internet_Explorer_box_model_bug).

[![](http://unchart.com/wp-content/uploads/2012/01/portalscreenshotmarked-300x190.png)](http://unchart.com/wp-content/uploads/2012/01/portalscreenshotmarked.png)

-------------

There are multiple ways to fix this. On the example above where the
Inbox flows wrong, this is the code that's broken:

    #ContentLeft {
       float: left;
       width: 20%;
       padding: 20px 0px 20px 20px;
    }
    #ContentRight {
       float: left;
       width: 79.5%;
       padding: 20px 20px 20px 30px;
    }

When this renders in a modern browser (with padding added on) it adds
up to more than **20% + 79.5% + Padding > 100%** and so it overflows down.

The quick hack (that then renders in all browsers correctly) would be
to switch to something like width: **70%** on #ContentRight.

There are several box model bugs on the page (look at the sidebar
boxes) so to fix everything a [developer would probably want to
reorganize the css](http://www.456bereastreet.com/archive/200612/internet_explorer_and_the_css_box_model/) rather than just hack the number like I mention above.

Without doing a complete portal design, a web developer could fix all the Portal Layout Bugs in a couple hours. I'd fix it myself, but I don't have access to the templates for portal. And I'm sure e-MDs isn't going to ask me. :-)

(Keep Reading: [Let's Encourage e-MDs to Fix Usability for Patients on Portal](http://unchart.com/2012/encourage-e-mds-to-fix-portal-usability/))
