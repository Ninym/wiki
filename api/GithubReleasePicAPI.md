---
title: Github Release下载次数图片生成API
description: 通过调用API来生成基于Matplotlib绘图的RELEASE下载次数饼状图
published: true
date: 2022-03-23T09:09:31.708Z
tags: github, pic, release, github release, generate, matplotlib, numpy
editor: markdown
dateCreated: 2022-03-17T03:25:49.463Z
---

# Github Release下载次数图片生成API

`https://dev.api.ninym.top/gh/release?author=${author}&repo=${repo}[&type=${type}]`

<div align='center'>
  
| Parameter | Description | Example | Required | Type | Default |
|:--:|:--:|:--:|:--:|:--:|:--:|
| `author` | The user/org of the repo | `GamerNoTitle` | √ | `Str` | None |
| `repo` | The name of the repo | `INVAXION-Unlocker` | √ | `Str` | None |
| `type` | The type of the api's return | `pic` | × | `pic` or `json` | `pic` |

</div>

从Github仓库的连接中，就可以得到`author`和`repo`，例如从`https://github.com/GamerNoTitle/INVAXION-Unlocker`可以得到`author`为`GamerNoTitle`,`repo`为`INVAXION-Unlocker`

由此得到链接`https://dev.api.ninym.top/gh/release?author=GamerNoTitle&repo=INVAXION-Unlocker`

默认返回为图片，就像下面这样

<div align='center'>
  
  ![](https://dev.api.ninym.top/gh/release?author=GamerNoTitle&repo=INVAXION-Unlocker)
  
</div>

当然你也可以返回带有一定数据的json，但是需要加入`type`这一个query参数，就像这样

`https://dev.api.ninym.top/gh/release?author=GamerNoTitle&repo=INVAXION-Unlocker&type=json`

返回值如下

```json
{
  "author": "GamerNoTitle", 
  "repo": "INVAXION-Unlocker", 
  "labels": ["CharacterUnlocker", "ThemeUnlocker"], 
  "downloads": [199, 245], 
  "pic": "https://dev.api.ninym.top/cache/GamerNoTitle-INVAXION-Unlocker.png", 
  "remark": "The access to the pic will be removed when the service is redeployed or by the operation of administrator"
}
```

<div align='center'>

| Parameter | Description |
|:--:|:--:|
| `author` | The user/org of the repo belongs to |
| `repo` | The name of the repo |
| `labels` | All the tags of the repo's releases |
| `downloads` | The download counts of all the release tags |
| `pic` | The link to the chart |
| `remark` | Just a notifiction |
  
</div>