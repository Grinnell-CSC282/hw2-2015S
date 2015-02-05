###Environment Variables written in Markdown
![](http://files.cyberciti.biz/cbzcache/3rdparty/terminal.png)

#####Def:
**environment variable: ** an environment variable is a value store on a computer, which can referred to one or programs. 

**NOTE: The system wide variable a stored in  /etc/profile **

######Display Current Variable

```
BASH
```
```
$ set
```
sample results:

```
BASH=/bin/bash
BASH_ARGC=()
BASH_ARGV=()
BASH_LINENO=()
BASH_SOURCE=()
BASH_VERSINFO=([0]="3" [1]="2" [2]="57" [3]="1" [4]="release" [5]="x86_64-apple-darwin14")

…
```

in C, one can get the variables by ——> **_Not sure, needs double checking_**
```
$ printf "%s\n" $HOME
```

######Display Current Variable

The [export command]() can be used to set env. variables.
For example one can set the PATH env. variable using the following command:

```
export PATH=${PATH}:/usr/sbin
```

The ~/.bash_profile can be edited to make the the changes permanent. 
Example (_Apparently I am the only one who likes Nano_):
```
$ nano ~/.bash_profile
```
Sample file content:

```
# Setting PATH for Python 3.4
# The orginal version is saved in .bash_profile.pysave
PATH="/Library/Frameworks/Python.framework/Versions/3.4/bin:${PATH}"
export PATH

```

edit save and close
#####Ref: 

* [_Cyberciti_](http://www.cyberciti.biz/faq/set-environment-variable-linux/)
* [_Wikipedia_](http://en.wikipedia.org/wiki/Environment_variable)

