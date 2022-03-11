---
title: 网易云音乐下载API
description: 可以通过调用API来下载网易云音乐的歌曲（注：无法试听的歌曲除外）
published: true
date: 2022-03-11T11:10:16.374Z
tags: netease, neteasecloudmusic, api, music, download
editor: markdown
dateCreated: 2022-02-11T04:26:38.356Z
---

# 网易云音乐下载API

### v1

`https://api.ninym.top/song/?id=${id}`

- `id` 音乐的id，可以通过网易云音乐的分享功能获得

### v2 (Unstable)

`https://dev.api.ninym.top/song?id=${id}[&type=(attachment | json)]`

`v2`在`v1`的基础上增加了一些query参数，这些参数如下

<div align='center'>

| Parameter | Example | Required | Type |
|:--:|:--:|:--:|:--:|
| id | `1472480890` | √ | `int`(any) |
| type | `attachment` | × |	`attachment`(default) or `json` |

 </div>
  
- `id`表示歌曲的id，可以通过分享链接获得

- `type`表示api的返回类型，如果是`attachment`则以文件方式返回，如果是`json`就会返回一个包含一定信息的json，下面是一个例子

```json
{
  "author": "YOASOBI", 
  "code": 200, 
  "link": "http://m10.music.126.net/20220311192740/ea6280394442dd75c7f54ab34955bf4a/ymusic/obj/w5zDlMODwrDDiGjCn8Ky/3695407857/774f/d95c/a844/40a2fce4c5077965a13c50d212f1a96a.mp3", 
  "msg": "Success", 
  "name": "\u7fa4\u9752"
}
```

### 通过分享链接获得id

例如[YOASOBI - 群青](https://music.163.com/song?id=1472480890&userid=252340012)这首歌

<div align='center'>
<img src='https://user-images.githubusercontent.com/28426291/153539463-24515417-4eb9-48b0-8c82-130649e40a9b.png' desc='获得网易云分享链接' />
</div>

通过网易云分享出来的链接为[https://music.163.com/song?id=1472480890&userid=252340012](https://music.163.com/song?id=1472480890&userid=252340012)

其中我们只需要`id=`后面的那一串数字，`userid`可以忽略掉



## Demo

[点我前往下载站](https://music.ninym.top)