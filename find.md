##GNU find

find is a very useful utility in bash, to search for files and directories. 
usage is simple

###to search all xml files in current directory
``` 
 #!/bin/bash
 find . -name "*.xml" 
``` 
###to search all xml files in the whole filesystem
``` 
 #!/bin/bash
 find / -name "*.xml" 
```
###to search and remove all xml files in the current directory
``` 
 #!/bin/bash
 find . -name "*.xml" -type f|xargs rm
``` 
###to search and copy file to another directory
```
 #!/bin/bash
find . -name "*.xml" -type f|xargs cp -t folder/
```
###send output of one process as command line arguments to another process
```
 #!/bin/bash
cat `find . -name "*.xml"` >> mergeAll.xml
```



