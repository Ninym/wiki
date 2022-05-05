---
title: 首页
description: 欢迎使用GamerNoTitle的API
published: true
date: 2022-05-05T12:47:59.096Z
tags: home, homepage, 首页, 主页
editor: markdown
dateCreated: 2022-02-11T04:14:27.076Z
---

# GamerNoTitle API Doc
欢迎使用GamerNoTitle提供的API接口，本网站是API的文档，你可以从左边选择你需要的API进行文档查询！

> 本项目开源仓库 [Ninym/api-flask](https://github.com/Ninym/api-flask)
{.is-info}

本API的地址如下

| Version | Link | Status | Backend | Mark |
|:--:|---|---|:--:|:--:|
| Main | https://api.ninym.top | Online | Python + Flask | Unstable, but more features |
| Legacy | https://legacy.api.ninym.top | Online | Javascript | Stable, but less features |

其中 `Main` 分支的分流如下（你可以通过访问[状态页面](https://status.ninym.top)来查看各服务的状态）

| Host | Link | Status | Mark |
|:--:|:--:|:--:|
| [Railway](https://railway.app?referralCode=U8coe_) | https://api.ninym.top \| https://railway.api.ninym.top | [![Better Uptime Badge](https://betteruptime.com/status-badges/v1/monitor/eb2i.svg)](https://betteruptime.com/?utm_source=status_badge) | Default |
| [Render](https://render.com/register) | https://render.api.ninym.top | [![Better Uptime Badge](https://betteruptime.com/status-badges/v1/monitor/eb2j.svg)](https://betteruptime.com/?utm_source=status_badge) |  |


> **本站需要登录才能够发表评论，如果你需要发表评论，请先登录！**
{.is-warning}


## 更新日志

- 2022.05.05 加入Osu代理下载API，可以通过此API加速你的osu谱面的下载，加入分流说明、在线状态显示
- 2022.03.23 将v1版本API归档为legacy，并使用新的域名指向v1版本，将v2版本列为正式版本，更改指向的域名。现在直接访问`https://api.ninym.top`将会使用v2版本的API（此次更新会出现短时间的证书错误，会自动恢复）
- 2022.03.18 加入Github Release下载圆饼图API
- 2022.03.11 加入网易云音乐下载API