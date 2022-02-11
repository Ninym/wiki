---
title: 网易云音乐下载API
description: 可以通过调用API来下载网易云音乐的歌曲（注：无法试听的歌曲除外）
published: true
date: 2022-02-11T04:54:58.726Z
tags: netease, neteasecloudmusic, api, music, download
editor: markdown
dateCreated: 2022-02-11T04:26:38.356Z
---

# 网易云音乐下载API

`https://api.ninym.top/song?id={id}.mp3`

## 变量解释

- `id` 音乐的id，可以通过网易云音乐的分享功能获得

### 通过分享链接获得id

例如[YOASOBI - 群青](https://music.163.com/song?id=1472480890&userid=252340012)这首歌

<div align='center'>
<img src='https://user-images.githubusercontent.com/28426291/153539463-24515417-4eb9-48b0-8c82-130649e40a9b.png' desc='获得网易云分享链接' />
</div>

通过网易云分享出来的链接为[https://music.163.com/song?id=1472480890&userid=252340012](https://music.163.com/song?id=1472480890&userid=252340012)

其中我们只需要`id=`后面的那一串数字，`userid`可以忽略掉

那么就可以通过访问[https://api.ninym.top/song/?id=1472480890](https://api.ninym.top/song/?id=1472480890)来下载到这一首歌曲。

## Demo

[点我前往下载站](https://music.ninym.top)