# Getting and Setting Environment Variables

## Using the Command Line or Bash

To get a variable we can simply say `echo $VAR_NAME`
- For example, `echo $PATH`
To set a variable name we simply VAR_NAME=INPUT
- For example, `LANGUAGE=en_CA:en`
We can also use env or printenv to list all the environment variables
- `printenv` or `env`

### Source(s) used:
- [Unix - Environment](http://www.tutorialspoint.com/unix/unix-environment.htm)
- [3.2. Variables](http://tldp.org/LDP/Bash-Beginners-Guide/html/sect_03_02.html)

## Using C

Getting environment variables in C can be accomplished by using the header file `stdlib.h`. 
Using `getenv` function: `char * getenv (const char *name)` will return the value of the variable `name`
  - For example, `getenv("PATH")`
  

### Source(s) used:
- [Environment Access](http://www.gnu.org/software/libc/manual/html_node/Environment-Access.html#Environment-Access)

