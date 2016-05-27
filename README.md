# Learning-bash

## use floating point variables in bash
example of while:

``` arg2=0.1
while (( $(bc <<< "$arg2 <= 1") ))
do
...
```

