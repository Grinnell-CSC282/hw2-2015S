##CSC-282 Homework 2
February 5th, 2015
Wesley Pollock

####1. Learn Markdown so that we can use it for these assignments.
* Did a quick [tutorial](http://markdowntutorial.com/).
* Redid my previous homework in markdown for practice.
* Now I'm writing this.

####2. Learn about how you set and get environment variables.
A quick discription of environment variables (found
     [here](http://www.ee.surrey.ac.uk/Teaching/Unix/unix8.html)):

>Variables are a way of passing information from the shell to programs when
 you run them. Programs look "in the environment" for particular variables
 and if they are found will use the values stored. Some are set by the
 system, others by you, yet others by the shell, or any program that loads
 another program.

>Standard UNIX variables are split into two categories, environment
 variables and shell variables. In broad terms, shell variables apply only
 to the current instance of the shell and are used to set short-term
 working conditions; environment variables have a farther reaching
 significance, and those set at login are valid for the duration of the
 session. By convention, environment variables have UPPER CASE and shell
 variables have lower case names. 

* `printenv`- Prints the current values for environment variables. 
  You can print the value of specific variables. For example, `printenv
 SHELL`.
* `env` - Lets you change the environment that programs run in.
* `set` - Allows you to read and write variables.
* `VAR_NAME=value` will set a shell variable.
  The shell variable is only available in the current session.
* `export VAR_NAME` will turn the shell variable into an environmental
  variable. 
* `export -n VAR_NAME` will change it back into a shell variable

#####List of Common Environmental and Shell Variables  
This list was copied from
[here](https://www.digitalocean.com/community/tutorials/how-to-read-and-set-environmental-and-shell-variables-on-a-linux-vps).

* `SHELL` - The shell that will be interpreting commands.
* `TERM` - Type of terminal to emulate when running the shell.
* `USER` - Current logged in user.
* `PWD` - Current working directory.
* `OLDPWD` - Previous working directory.
* `MAIL` - Current user's mailbox.
* `PATH` - Directories systems checks for commands.
* `HOME` - Current user's home directory.

##### Login vs Non-Login
* A login session attempt to read from `~/.bash_profile`, `~/.bash_login`,
and then `~/.profile`
* A non-login session will read `/etc/bash.bashrc` then the user-specific
`~/.bashrc`
  You can define user-specific environemntal variables, available in both
  login and non-login shells, in the `~/.bashrc` file:
        * `export VAR_NAME=value` - will set the environmental variable.
        * `source ~/.bashrc` - will make the current session read the file
        to apply changes. 
            
####3. Come up with two or three tasks, similar to those we did for assignment 1, and put notes about them in the tasks directory. (You can include some sample solutions in your file.)


