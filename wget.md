##wget 
it is a free software package to download files using http/https or ftp. most of the times, we want to download files:

```
wget $filename
```

###download directories without index.html
```
 wget -r --no-parent --reject "index.html*" $url/
```
