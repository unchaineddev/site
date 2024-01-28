---
title: "mpv scripts"
date: 2023-09-18T08:36:10+05:30
draft: false
tags: ['linux']
---

in this blog, i will share a list of no-nonense scripts for mpv. 

if you are not using mpv, and using something else -- here are few reasons why you must consider it:

- lightweight
- customizable with scripting support
- relatively easy to setup and use
- faster than vlc

# Scripts

#### 1. mpv chapters[^1] 

- Display chapters and allow you to jump to them with a mouse click.
- <i>as easy as saving the file in your `scripts/` folder.</i>
- press *TAB* to display the chapters.


{{< figure src="/blog/mpv-chapters.png" thumb="-thumb" size="1442x662" caption="https://github.com/zxhzxhz/mpv-chapters" caption-effect="none" >}}


#### 2. mpv thumbnails script[^2]
\
Display preview thumbnails when hovering over the seekbar.


{{< figure src="/blog/mpv-thumbnails.gif" thumb="-thumb" size="1442x662" caption="https://github.com/marzzzello/mpv_thumbnail_script" caption-effect="none" >}} 

##### Setup

- copy the 2 scripts from the [releases page](https://github.com/marzzzello/mpv_thumbnail_script/releases) and place them in your config file: ```$HOME/.config/mpv/scripts/```
- set 'osc=no' or un-comment the link in your mpv.conf file in the path ```$HOME/.config/mpv/mpv.conf``` 


If you want to take a look at other user scripts, you can view them [here](https://github-wiki-see.page/m/mpv-player/mpv/wiki/User-Scripts)


[^1]: https://github.com/zxhzxhz/mpv-chapters
[^2]: https://github.com/marzzzello/mpv_thumbnail_script
