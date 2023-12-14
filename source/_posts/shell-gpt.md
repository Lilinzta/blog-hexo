---
title: shell_gpt
date: 2023-08-26 16:24:01
tags: Share
---
## 由 GPT-3 和 GPT-4 提供支持的命令行生产力工具将帮助您更快、更高效地完成任务。
<!--more-->
> Tips: 下面都是废话，可以直接看这两个链接：[GPT_API_free](https://github.com/chatanywhere/GPT_API_free)和[shell_gpt](https://github.com/TheR1D/shell_gpt)

## 获取一个免费的GPT_API
点击第一个链接，获取免费的GPT_API，当然也可以付费获得更好的体验。

与官方的API使用步骤基本相同，需要额外设置代理，具体使用可以详细阅读文档。

## shell_gpt使用GPT_API_free
第二个链接，使用方法说的很详细。配置文件在`~/.config/shell_gpt/.sgptrc`,需要配置(修改)以下两个变量:
```
OPENAI_API_KEY=领取的免费API(一般为sk-开头)
OPENAI_API_HOST=https://api.chatanywhere.cn 或者 https://api.chatanywhere.com.cn
```