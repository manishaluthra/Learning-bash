# Learning-bash
## incrementing 
There are many ways to increment a variable in bash. Most frequently most of the times we do `i++`. But, this is incorrect. Correct interpretation is:

```
#!/bin/bash
i=0
...
((i++))
```

Or, it also provides `let` command for the same. But, be careful you have to enable it first. [Here's](http://ubuntuforums.org/showthread.php?t=1377218) how you can do that. Some of the example to increment a variable using let:

```
#!/bin/bash
...
i=0
let ++i
let "i=i+1"
```

## different usage of for loop
```
#!/bin/bash
...
for i in 1 2 3 4 .. N
do
...
```

latest version (bash version 3.0+) supports range for loops, example:
```
#!/bin/bash
...
for i in {1..5}
do
...
```

## use floating point variables in bash
Bash do not allow floating point numbers in the script, but can process *only* integers in a _plain_ manner. Though, allows its usage by `bc` command. Basically its a precision calculator language, which also provides support of standard math library.
example of its usage in while loop:

``` 
#!/bin/bash
...
arg2=0.1
while (( $(bc <<< "$arg2 <= 1") ))
do
...
```
same usage goes in if loop:

``` 
#!/bin/bash
...
if (( $(bc <<< "$arg2 <= 1") ))
		then
```
##adding floating point numbers to your variables
example:
``` 
#!/bin/bash
...
incl=0.02
arg2=0.2
arg2=`echo $arg2 + $incl | bc`
```
