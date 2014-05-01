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


### Example One

You have a tab-delimited text file, gene_exp.txt that contains data from a differential gene expression analysis

#### Step one, investigate  the file 

What is the file structure? Without options, ***head*** will print the top 10 lines of the file

<pre>
$ head  gene_exp.txt
gene	sample_1	sample_2	status	value_1	value_2	significant
AT1G01010	WT	hy5	NOTEST	0	1.49367	no
AT1G01020	WT	hy5	NOTEST	7.27837	10.7195	no
AT1G01030	WT	hy5	NOTEST	1.18638	1.10483	no
AT1G01040	WT	hy5	NOTEST	0.239843	2.24208	no
AT1G01046	WT	hy5	NOTEST	0	0	no
AT1G01050	WT	hy5	OK	9.06975	23.5089	yes
AT1G01060	WT	hy5	NOTEST	4.04534	6.46964	no
AT1G01070	WT	hy5	NOTEST	1.24918	2.41377	no
AT1G01073	WT	hy5	NOTEST	0	0	no
</pre>

The header line describes the columns for us.  WE can use this to help answer some questions.


