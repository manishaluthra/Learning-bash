# Learning-bash

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
example of while loop:

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
