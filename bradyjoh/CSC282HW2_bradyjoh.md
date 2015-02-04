John Brady
CSC282, Rebelsky
Homework 2
February 5, 2015

1. Learn Markdown so that we can use it for these assignments.
	Source: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
	Inline `code` has `back-ticks around` it.
	```Blocks of code are surrounded by 3 back-ticks ```
	>Start a line with a greater-than for a quote

	Two newlines for a new paragraph
	or one line for the same
	Pound sign # before a heading. Can do 1-6 for varying size. Put '-' or
	 '=' underneath for line separator

	 One set of asterisks on either side gets italic, and two asterisks get **bold**
2. Learn about how you set and get environment variables.

2a. Command line
	Assuming Windows CLI, 'SET' will return the environment variables. To set,
	use 'setx <newpath> /m' or 'set <pathname>=<newpath>'
	From http://stackoverflow.com/questions/21606419/set-windows-environment-variables-with-commandline-cmd-commandprompt-batch-file
2b. Bash
	'printenv' to see all the variables. 
	add to '.bashrc' file, which stores all environment variables
2c. C (get only)
	'char * getenv' to get environment variables in C. Part of stdlib.h. 

3. Come up with two or three tasks, similar to those we did for assignment 1, 
and put notes about them in the tasks directory. (You can include some 
sample solutions in your file.)