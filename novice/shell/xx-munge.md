---
layout: lesson
root: ../..
title: Data mining text files on the unix command line
---

### Motivation
In many fields, you will encounter data stored in text files.  For complex text parsing and re-formatting tasks, it might be a good idea to use or write a shell script, python script, etc. that simplifies the job.  However, if the file format is structured (tab-delimited, comma-delimited) and you want to do a quick, ad-hoc data extraction, it can sometimes be easier to use some simple, command-line  data mining techniques to get what you need in less time than it would take to write a script.


### Objective

Learn to use a simple set of unix command line tools to to quick and dirty data extraction from commonly encountered tect file types.

### Your toolkit

_Subject_ __Hello__ World!

    $ code 1 $hello;



#### Filtering

Select only data meeting a condition:

    SELECT * FROM table_name WHERE column_name > 0;


#### Missing Data


Test whether a value is null:

    SELECT * FROM table_name WHERE column_name IS NULL;

