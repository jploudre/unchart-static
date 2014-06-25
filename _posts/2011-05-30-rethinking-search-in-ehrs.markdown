---
author: jploudre
comments: false
date: 2011-05-30 16:57:37+00:00
layout: post
slug: rethinking-search-in-ehrs
title: Rethinking Search in EHRs
wordpress_id: 743
categories:
- software
- theory
tags:
- e-MDs
- simplicity
- usability
---

Let's take a stroll down memory lane for a moment. In the mid-1990s the Web exploded into mainstream. It started with a few sites with academic papers, recipes, jokes, etc. Suddenly it had more information than you could possibly get to. The rapid change in complexity was astounding. Into that spot came one of the early iconic Web companies. Yahoo. (Aside: Before they went public, they had a contest to create a marketing tagline. They gave away 50 baseball caps to their favorite entries. I still have mine. My entry -- "Yahoo, wasting time made efficient.")

Here's how Yahoo tamed  complexity over 15 years:

![](/files/2011/05/3786863152_31559284df_m.jpg)![](/files/2011/05/3786863254_8549fdb860_m.jpg)![](/files/2011/05/3786863674_629e018e07_m.jpg)

Ok, I cheated. I skipped from 1995 to 2009 between the second and third screenshoot. But the trend is clear. What started as a way to tame complexity is now itself complex. So, although this designed (it's not pure entropy), there's clearly a limit on how much information we can access through a directory.

In my clinic, we use a primary ordering template. It's got a Yahoo problem -- we have 3000 items in the template. Even when you know the template like the back of your hand, it takes real time and attention to navigate through. There are limits to usability as size increases. You can manage this somewhat through good [information architecture](http://en.wikipedia.org/wiki/Information_architecture). 

e-MDs main solution to this complexity is templates. You can create hierarchical templates that allow you to delve down and select items. Personally I think templates are their most successful custom widget. e-MDs created a number of non-standard interface widgets with varying degrees of success. So while having free text insertion everywhere has some flexibility, the darn free text widget ![](/files/2011/03/freetext.png) is too small and difficult to select.

Templates were designed for tablet use and if you never need to use a keyboard, the template is impressive in it's speed. (Tablet mode never worked for me becuase I need to enter text regularly and handwriting was inefficient and frustrating. Flipping back and forth between tablet and laptop mode didn't really work for me) It's essentially a group of buttons that are ~ 200 by 25 pixels. That's  big enough to be easily tappable (especially compared to the 6 by 6 pixels of "free text".) e-MDs was designed when [XGA was the most common display standard](http://en.wikipedia.org/wiki/Computer_display_standard). 1024 x 768 is still a common resolution -- my iPad uses it, for example. You lose usable space by all the chrome around the information (See: [Interface Janitor](/2011/e-mds-interface-janitor/)) Still, you can fit 4 columns of 25 buttons -- 100 could be on the screen at once. If you had a perfect outline, a 2 layer hierarchy  could hold 625 items, a 3 layer could hold 15K items. 

###Thinking about Search

So much for hierarchy. Now let's think about Search as Interface. I think we can agree what internet company to look at. Here's Google's 1997 and then 2009 homepage.
![](/files/2011/05/1997-300x181.jpg)
![](/files/2011/05/google-2009-fade-in-large-300x168.png)

Boy, that really hides the complexity! Interestingly, Google's gotten much better during that interval -- it's faster than ever to use. It corrects for human constraints. Typos, for example. Or slow typing -- Google Suggest adds autocompleting to search terms so you don't have to type as much. [Google Instant](http://www.google.com/instant/) goes even further by doing the navigating while you are still typing. They say that saves 2-5 seconds per search. So that same box gets more powerful and quicker-to-use at the same time.

If you put it in strategic terms, Google aims to simplify complexity so users can get back to what they are trying to do. Contrast that with a screenshot from e-MDs. So, 6  characters into hypertension (by far one of the most common chronic disease), and how are things looking:

![](/files/2011/05/Screen-shot-2011-05-30-at-9.31.26-AM.png)

###Stop disrespecting doctors!

This shows a lack of insight about search and modern software. Seriously: Why do you have to designate 'Search by' options? A computer from 10 years ago could easily handle all 4 searches and merging the results into a single list. A couple megabytes of data at most. If you type in a number, you're clearly doing a CPT search. **Don't make us think.** Even though the system has practice-specific ICD frequency data -- it doesn't use that to sort results. No, it uses ICD codes in numerical order. 'Cause that makes a lot of sense for a doctor providing care. Disrespectful. Or couldn't it automatically fallover to the full search if your short search fails? Use a common abbreviation (HTN) and how does that work?

There's a science behind this. I think the book [Search Patterns](http://searchpatterns.org/library.php) get's it best. It explains common design patterns and user behaviors. This isn't something where EHRs have to create a new field of understanding. Dealing with complexity is bread and butter for all knowledge workers. Rather EHRs need to learn to apply best practices pervasively. It's a respect for the importance of what's going on here. If it was your health, would you want a time-limited Doc using Yahoo or Google? Doctoring is sacred work and we're hoping that tech-enabled care can allow doctors to  transcend some of our own limits (like memory or handwriting quality.) But we're getting tech-encumbered care (hold on, I've got to click about six or seven things before I can pay attention to you.) The tech gives us new powers but always extracts tradeoffs by distracting us or making work more complicated.

Search isn't *the answer*. But it's one of the answers.

