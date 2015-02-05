# Week 2 Stuff
## Environment variables

### In Command Line
To print every environment variable currently defined, enter `printenv`, or
if you want a particular one, you can enter `printenv | grep 'var'`, which
will narrow your search.

To set an environment variable one can input
```bash
export VARNAME=stuff
```

[Source](http://www.cyberciti.biz/faq/set-environment-variable-linux/)


### In C
The procedure
```c
char * getenv (const char * name);
```
found in the `stdlib.h` library allows you to access the value
of an environment variable by giving its name as input. Also, the
procedure
```c
int system (const char * string);
```
in the same library "allows a C program to run another program (possibly
an operating system command)". King gives the example
```c
system ("ls >myfiles")
```
for a *nix-type program command. You can use `system()` and a choice
of command-line options to set environment variables in C (although I'm sure
there's a more direct way).

Source: K. N. King. _C Programming: A Modern Approach_. (2008).


## Some tasks that *nix can solve
The first idea I had was to write a script that, given an `HTML` file, 
check to see that the number of `<div`s matches the number of `</div>`s.
My solution is (an inelegant) stream of commands:
```bash
open_div=$(grep -o '<div' filename | wc -l);
close_div=$(grep -o '</div>' filename | wc -l);
echo "<div> count: $open_div";
echo "</div> count: $close_div";
if [ $open_div == $close_div ]; then echo "they match"; fi
```
[Source 1](http://stackoverflow.com/questions/7119936/results-of-wc-as-variables) and 
[Source 2](http://www.theunixschool.com/2012/10/how-to-find-total-count-of-word-string.html).

The second idea I had was a bit simpler: take the 10 most memory-intensive 
active processes and write them to a file. To solve this one, I simply did
```bash
ps aux --sort%mem | head -11 > filename
```

which writes all of the info to `filename`. The thing I don't like about this solution
is that if you are running Google Chrome for example, the `CMD` entry given in `ps` is
this massive path name that screws up the otherwise neat formatting. I don't know how to
fix this, but otherwise it works as I wanted it to.

[Source](http://www.cyberciti.biz/faq/show-all-running-processes-in-linux/).
