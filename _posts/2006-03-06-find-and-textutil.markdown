---
author: jploudre
comments: true
date: 2006-03-06 17:15:26+00:00
layout: post
slug: find-and-textutil
title: Find and textutil
wordpress_id: 266
categories:
- software
tags:
- macro
- proofofconcept
---

I recently had a huge folder of word documents that I wanted to make into text documents. Unfortunately they were spread in a number of subfolders. Since there were about 36K files, I sure didn't want to do this manually. (I was going to use these files to setup Dragon Naturally Speaking.)

Mac OS X 10.4 has a function called textutil that allows conversion between different types of files. So what I needed was a way to feed it the name of every file. As it turned out, the solution was relatively short and sweet. This is the power of command line.

     find . -name *.doc -exec textutil -convert txt '{}' \; 


|Command:|What it does:|
|--------|---------|
|find|a unix command for directory recursion|
|.|the current folder|
|name *.doc|every .doc file|
|-exec|apply a shell command|
|textutil -convert txt|convert it to a text file|
|'{}'|the filename from the find command|
|\;|the end of the -exec command above.|

Combining the find command with textutil makes it a power utility.

     find . -name *.doc -exec rm '{}' \;

Can be used afterwards to remove all the .doc files.
