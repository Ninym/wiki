---
title: Osu谱面代理下载
description: 通过api来帮助你加速下载osu的谱面
published: true
date: 2022-05-05T11:30:08.719Z
tags: download, osu, downloader, map, osz
editor: markdown
dateCreated: 2022-05-05T11:18:55.209Z
---

# Osu谱面代理下载

`https://api.ninym.top/beatmapsets/${mapid}(?noVideo=${noVideo})`
`https://api.ninym.top/osumap/${mapid}(?noVideo=${noVideo})`

**上面这两个路径都可以访问到这个api**

<div align='center'>

| Parameters | Description | Example | Required | Type | Default |
|:--:|:--:|:--:|:--:|:--:|:--:|
| `mapid` | The id of the map | `1965653` | √ | `int` | None |
| `noVideo` | Whether the map should contain the video | `0` for yes or `1` for no | × | `int` | If the map contain a video, than the value is `0`, otherwise this will not work |

</div>

`mapid`可以从谱面的链接中看到，例如[谱面链接](https://osu.ppy.sh/beatmapsets/941246)`https://osu.ppy.sh/beatmapsets/941246`，从这个链接中可以知道`mapid`是`941246`

这个API只会返回谱面文件，没有任何的json返回。目前没有对`mapid`进行合规性判定

## 举个栗子

在谱面链接`https://osu.ppy.sh/beatmapsets/941246`中，直接将`osu.ppy.sh`改成`api.ninym.top`，浏览器直接开始下载谱面文件

https://osu.ppy.sh/beatmapsets/941246 -> https://api.ninym.top/beatmapsets/941246