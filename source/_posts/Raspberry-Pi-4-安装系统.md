---
title: Raspberry Pi 4 安装系统
date: 2023-12-12 22:42:36
tags: Raspberry Pi 4
---
最近入手了一个树莓派4B 4GB, 分享一下在安装操作系统时的经验.
<!--more-->
## 1.官方推荐方式
下载官方的烧写工具，它会自动替你下载镜像文件，还支持添加一些自定义配置，比如用户名和密码，wifi 和 ssh.

适合只有一台电脑和一个树莓派的情况.

> 我是因为校园网的原因，只能使用电脑开热点，让树莓派去连.

如果你在 GNU/Linux 下开热点遇到困难，可以参考我的这个脚本(很久之前网上找的)，如果你有更好的方式，也欢迎在评论区留言.
```sh
#!/bin/bash
sudo iw phy phy0 interface add wlan0_ap type managed addr 12:34:56:ab:cd:ef

sudo create_ap -c 11 wlan0_ap wlan0 NAME PASSWD >/dev/null &
```
## 2.安装其它的GNU/Linux ARM 版本
文档都很详细，我就不多说了.
### [Kali Linux ARM](https://www.kali.org/docs/arm/raspberry-pi-4/)
### [Arch Linux ARM](https://archlinuxarm.org/platforms/armv8/broadcom/raspberry-pi-4)
## 3.TODO
32bit 和 64bit 的系统都试过，目前还没有通过HDMI接显示器进入过桌面环境.

放假回家之后树莓派能直接插路由器上，就能装 Arch Linux ARM 了😀.