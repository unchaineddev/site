---
title: "Archiving Files Using Tar"
date: 2023-11-09T19:46:04+05:30
draft: false
tags: ['linux']
---


I like archiving files and directories, mostly due to local storage constraints. Creating backups of files and saving them in tarballs or 7zips has become second nature to me. However I have realized I have been doing it wrong all along. I've predominantly relied on GUI methods, only to discover that the command line method is so straightforward that even a caveman could do it.

This is a short note for me, and for you in case you would want to compress or extract archived files using the command line.


1. __Creating a Tar Ball__


```shell
tar -cvf project.tar /path/to/files  # does not compress
```  

    
2. __Compressing a Directory__


```shell
tar -czvf project.tar.gz /path/to/files
```


3. __Extracting All Files__


```shell
tar -xf project.tar
```


4. __Listing Contents in Tar File__


```shell
tar -tvf project.tar.gz
```


5. __Finding Specific File in Tar File__


```shell
tar -tvf project.tar.gz "path/to/file"
```


6. __Extracting One file from Tar__


```shell
tar -zxvf project.tar.gz "/path/to/file"
```

<hr>


OPTIONS:

- --c  create an archive
- --f specify file
- --t list contents without extracting archive
- --v verbose; displays progress in the terminal
- --x extracts files
- --z compress with gzip
