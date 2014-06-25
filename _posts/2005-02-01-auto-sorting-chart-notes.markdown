---
author: jploudre
comments: true
date: 2005-02-01 17:11:49+00:00
layout: post
slug: auto-sorting-chart-notes
title: Auto-sorting Chart Notes
wordpress_id: 262
categories:
- software
tags:
- efficiency
- gtd
- macro
- proofofconcept
---

Has this ever happened to you? A patient comes in to tell you about a problem, and, golly, they don't tell you the story in the order that you want to chart it. The patient tells you some HPI, then mentions a bit of social history, skips to medical history and goes back to the HPI. In one sentence.

I mentioned this problem to some acquaintances who use [BBEdit](http://barebones.com) and one of them whipped out a short [perl](http://perl.com) script that auto-sorts the note.

It's pretty simple, I defined some 'tags' that I type to determine what type of information it is. (Actually, I'd use something like [typeit4me](http://typeit4me.com/) to make `sh` turn into `SocHx:`.

The script assumes that untagged lines go with the previous tag.

And it works. It's better than an autosorting feature built-in to things like Micorsoft Word because you can easily edit how things will sort. And it only sorts if you tell it to. This is definitely a 5 star idea. I may port this over to [Vim](http://www.vim.org) at some time. 

	#!/usr/bin/perl -w
	use strict;
	my %list = (  
				  ''       => 0,
				  'CC'    => 1,
				  'HPI'     => 2,
				  'ROS'    => 3,
				  'MedHx'	=> 4,
				  'SurgHx' => 5,
				  'FamHx' => 6,
				  'SocHx' => 7,
				  'DevHx' => 8,
				  'ObHx' => 9,
				  'PEX' => 10,
				  'Dx' => 11,
				  'Rx' => 12  
			   );
	my $currentState = '';
	my %storage = ();
	
	while (defined (my $line = <>)) {
		chomp( $line);
		if ($line =~ m/^\s*([^\:]*)\:\s*(.*)$/) {
			if (defined $list{$1}) {
				$currentState = $1;
				$line = $2;
				if ($line =~ m/^\s*$/) {
					next;
				}
			}
		}
		
		if (! defined $storage{$currentState}) {
			$storage{$currentState} = [ $line ];
		}
		else {
			push ( @{$storage{$currentState}}, $line);
		}
	}
	
	foreach my $key ( sort { $list{$a} <=> $list{$b} } keys %storage) {
		if ($key ne '') {
			print "\n", $key, "\n";
			print "-"x(length $key), "\n";
		}
		print join( "\n", @{$storage{$key}}), "\n";
	}

-----

*2011 Update* Dealing with out-of-order information is still a huge problem. All day long I'm flipping back and forth inside the chart. A little better with macros but still a pain.

