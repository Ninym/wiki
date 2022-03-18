---
title: Github Release下载次数图片生成API
description: 通过调用API来生成RELEASE下载次数饼状图
published: true
date: 2022-03-18T02:04:10.763Z
tags: github, pic, release, github release, generate, matplotlib, numpy
editor: markdown
dateCreated: 2022-03-17T03:25:49.463Z
---

# Github Release下载次数图片生成API

`https://dev.api.ninym.top/gh/release?author=${author}&repo=${repo}[&type=${type}]`

| Parameter | Description | Example | Required | Type | Default |
|:--:|:--:|:--:|:--:|:--:|
| `author` | The user/org of the repo | `GamerNoTitle` | √ | `Str` | None |
| `repo` | The name of the repo | `INVAXION-UNLOCKER` | √ | `Str` | None |
| `type` | The type of the api's return | `pic` | × | `pic` or `json` | `pic` |

