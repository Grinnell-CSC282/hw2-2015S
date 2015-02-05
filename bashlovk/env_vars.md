# Getting and Setting Environmental Variables
## Using Command line 
### Get
  * Print out all environmental variables  
    * `printenv`
    * `env`
    * `set` (more vars and in alphabetical order)
  * Print out individual variables
    * `echo $*`  
    _Example:_ `echo $PATH`

### Set
   * `export VAR="new_var"`  
   _Example:_ `export MAIL="grinnell@grinnell.edu"`

## Using Bash
Viewing and modifying environmental variables from a bash script is basically
the same as from command line.

### Get
  `echo $*`  
 _Example:_ `echo $EDITOR`

### Set
 `export VAR="new_var"`  
 _Example:_ `export PATH=$PATH:/opt/bin:/usr/local/bin:$HOME/bin`

## Using C

### Get
Use [**getenv**][getenv man], for instance:  
`char * env_var = getenv("LANG");`

### Set
Use [**setenv**][setenv man], for instance:  
`setenv ("EDITOR", "vim", 1);`


_Sources about [environmental variables in bash][unix craft] and 
[in C][lemoda]_
[unix craft]: http://www.cyberciti.biz/faq/set-environment-variable-unix/
[getenv man]: http://man7.org/linux/man-pages/man3/getenv.3.html
[setenv man]: http://man7.org/linux/man-pages/man3/setenv.3.html
[lemoda]: http://www.lemoda.net/c/set-get-env/
