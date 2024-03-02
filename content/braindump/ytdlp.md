+++
title = 'Best way to download Youtube Videos'
date = 2024-02-17T09:09:37+05:30
draft = false
+++

There was a time when it became incredibly difficult to make yt-dl work,due to several takedown notices from youtube. From personal experience, if it worked for me once, it wouldn't work for the rest. It was frustrating to use third-party ad-ware sites to download anything off youtube.. until I discovered a (fork of yt-dl) better tool: __YT-DLP__. 

It is one of those things that makes me really admire the efforts of the open-source community. In this post, I will share my go-to commands for using yt-dlp.


## Install

```shell
sudo wget https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp -O /usr/local/bin/yt-dlp
sudo chmod a+rx /usr/local/bin/yt-dlp
```


## Usage

- Download and merge the best video-only format and the best audio-only format, or the best combined format (if video-only format is not available)

```shell
$ yt-dlp -f "bv+ba/b" <link>
```


- Download a video in 1080p

```shell	
yt-dlp -f 'bv*[height=1080]+ba' <link>
```

- Download an audio while embedding thumbnail in the file. 


```shell
yt-dlp -x --audio-format best --embed-thumbnail <link>
```


## Alias

- Obviously you can add this as an alias in your .bashrc or your .zshrc like so:

```shell
alias yta="yt-dlp -x --audio-format best --embed-thumbnail"
```

<hr>

YT-DLP's Github: [{{< icon "github" >}}](https://github.com/yt-dlp/yt-dlp) 
