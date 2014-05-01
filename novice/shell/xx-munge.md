---
layout: lesson
root: ../..
title: Data mining text files on the unix command line
---

### Motivation
In many fields, you will encounter data stored in text files.  For complex text parsing and re-formatting tasks, it might be a good idea to use or write a shell script, python script, etc. that simplifies the job.  However, if the file format is structured (tab-delimited, comma-delimited) and you want to do a quick, ad-hoc data extraction, it can sometimes be easier to use some simple, command-line  data mining techniques to get what you need in less time than it would take to write a script.


### Objective

Learn to use a simple set of unix command line tools to to quick and dirty data extraction from commonly encountered tect file types.

### Level

This is a novice-to-intermediate level lesson.  It is assumed that you know the unix command line basics.

### Your toolkit

This is a list of a few command that we will use in the examples below. 

<table>
  <tr><th>|</th><td><i>strings together the inputs/outputs of a series of commands</i></td></tr>
  <tr><th>grep</th><td><i>searches for patterns in text</i></td></tr>
  <tr><th>sort</th><td><i>orders lines in text</i></td></tr>
  <tr><th>head</th><td><i>prints the top N lines of text</i></td></tr>
  <tr><th>tail</th><td><i>prints the bottom N lines of text</i></td></tr>
  <tr><th>uniq</th><td><i>reports or filters repeated lines of text</i></td></tr>
  <tr><th>wc</th><td><i>counts words, characters or lines</i></td></tr>
  <tr><th>bc</th><td><i>does simple math on the command line</i></td></tr>
</table>


#### Filtering

Select only data meeting a condition:

    SELECT * FROM table_name WHERE column_name > 0;


#### Missing Data


Test whether a value is null:

    SELECT * FROM table_name WHERE column_name IS NULL;

