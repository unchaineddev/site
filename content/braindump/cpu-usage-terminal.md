+++
title = 'How to check CPU Usage in the Terminal?'
date = 2024-02-11T18:31:46+05:30
draft = false
tags = ["linux"]
+++

I like to optimize my system's performance and like it even more if the cpu usage is at the bare minimum. To me these commands are a must for system administration and performance monitoring. 


### Display all CPU information

```shell
cat /proc/cpuinfo
```

### Shows CPU usage

```shell
grep "cpu MHz" /proc/cpuinfo
```

### Updates CPU usage every 2s
```shell
watch  grep \"cpu MHz\" /proc/cpuinfo
```


### Watches CPU usage every 1s 

```shell
watch -n 1 grep \"cpu MHz\" /proc/cpuinfo
```
