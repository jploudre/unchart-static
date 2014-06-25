---
author: jploudre
comments: false
date: 2011-05-06 16:53:25+00:00
layout: post
slug: peak-versus-sustained-charting
title: Peak versus Sustained Charting
wordpress_id: 703
categories:
- theory
tags:
- e-MDs
- efficiency
- usability
---

This week I had a conversation with a medical transcriptionist who's struggling with her new job. The company that just took over has an 'On-the-job' clock but also has a 'Transcribing window open' clock. She feels a pressure to try to make them match -- 8 hours of work should be 8 hours of transcription. Since she's a human (not a computer or machine) that's completely unrealistic. 1 bathroom break in 8 hours: failure. Even if you consider labor laws -- 15 minute breaks and a lunch -- it's impossible to sustain attention that long.

In medical transcription, they often judge performance in lines/hour. A line is 60-70 characters (with or without spaces counted, depending on the company). 350 lines/hour is pretty solid work so it ends up a sustained rate of something like 75 wpm in typing terms. Nowadays, many medical transcriptionists are actually doing editing of computer transcription. They aren't allowed to use abbreviations to expand their word count. So 'COPD' doesn't expand into 'Chronic Obstructive Pulmonary Disorder' to get extra lines. On a good dictations, she might get to 1.7 real time. 

Interestingly enough, it seems lately that the radiologists are working like the transcriptionists -- **editing**. I had a patient this week with flank pain and I ordered a CT-KUB. The result didn't arrive like it was supposed to so I went onto our PACS system. I found the study, there wasn't yet the full report but the audio was there. When I clicked I heard the radiologist say: *"See the approved Tech's Report."* And a little later a 1 page document with the 6mm stone and mild hydronephrosis showed up. So apparently hydroneprhosis is a tech-level documentation that gets confirmed by the radiologist.

So the CT report shows the limits of *Peak Charting*: After all the thinking/evaluation/etc, a page can be dictated in 5 words. Honestly, if the radiologists worked at it, it could be a single character (Checkmark!) But no radiologist is just saying checkmark, checkmark, checkmark. The thinking/examining takes lots of real time so sustained charting is dramatically slower. And on complicated scans the dictation probably slows to something like 100-150 words per minute.

### Peak Charting in e-MDs

Peak charting for me would be a routine cold. My roomer might have used a shortcut, entered the HPI/Vitals, there's a basic exam and plan. Assuming it's a complete cookie cutter visit, I could theoretically just sign-off. In my macro-enabled world, I'd hit one macro to close to the E&M; coder, glance at it to check, then hit enter, look at my note conclusion printing options, and hit my signoff macro. On a visit like this in the middle of the day, that's actually about 5 seconds.

The visit, of course, lasts much much longer. There's small talk, figuring out what the patient is actually worried about, examining, educating, etc. And I usually try to add a little '[narrative](/2011/using-dragon-with-e-mds/)'. So, I'll type a sentence or two into the HPI to amplify. And I'll update some social history. Still my peak charting will still be well under a minute for a simple single-problem visit.

Sustained Charting is harder to measure. On a couple problem visit (both easy/routine problems), navigating back and forth eats up real time. I might be able to use a preclick ROS, say, but I need to add a few more for the second problem. Same thing with the exam. And if I'm finishing up the plan (aiming for real time, if I want finished visit summary), there's jumping back and forth between plan templates to describe discussions, medications, followup, testing.

What I used to do was open the free text after an assessment and type something like, "fu1w inip. dsal. dholdabx." And with the magic of autohotkey and my abbrevation efforts in the past few years, out would pop "Follow up in 1 week if not improving. Discussed and demonstrated use of saline sinus lavage for symptom reduction. Prescribed antibiotics but a plan to hold and monitor symptoms for now." So something like 7 seconds typing. And a second or two to click on the right ![](/files/2011/03/freetext.png)

I'm now trying to keep plan as 'structured data' inside a template since that's the current requirement for having it print in the visit summary. It takes me longer than a narrative blob with abbreviations like above. If I typed 10 words a minute, templating might be faster. More than time, though, it takes attention. Once I have the freetext open, I can lift my eyes from the screen and glance at the patient. (That's Touchtyping!) There's no reading or finding involved. With selecting on a template, there's finding the right template, finding the followup button, finding the discussions button, etc. I know I could optimize that with preclicks (and editing to match my plan) but it's a [local maximum again](/2011/how-much-time-can-macros-save/).

For faster Sustained Charting, jumping back and forth needs to be quicker (without focused attention.) And I need a way to generate lots of structured data (without focused attention). The jumping I've got covered with macros:

1. F1 jumps to ROS template
2. F2 jumps to exam template
3. F3 adds a diagnosis
4. F4 (on hiatus, used to prescribe via the health summary, but that doesn't document right.)
5. F5-F8 jumps to the plan template for the first through fourth problems.

Generating structured data without focused attention is harder. I think the best model is autocompleting like the location bar in a web-browser. That could behave a lot like a free text blob. I can leverage abbreviations I know (CBC could order the lab....)  so it wouldn't be hard to use. But hacking this on top of our templates is inelegant. I'm definitely not going to parse the template XML. This is something that would be much better built-in. I probably will create it for my purposes but it'll never be something I could release for wider usage.

I can do notes in near real-time but it changes me into the patient's data entry technician. I need a way to get the work done but limit the impact/focus on charting so I can focus on the person instead.

