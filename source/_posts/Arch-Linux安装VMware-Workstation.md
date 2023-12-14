---
title: Arch Linux安装VMware Workstation
date: 2023-08-07 08:43:57
tags: Arch Linux
---
# Arch Linux从AUR源安装VMware Workstation
<!--more-->
更完整的安装说明请参考 [Arch Wiki](https://wiki.archlinuxcn.org/wiki/VMware)
### 1.安装依赖
```sh
sudo pacman -S fuse2 gtkmm linux-headers ncurses libcanberra pcsclite
```
### 2.安装VMware Workstation
```sh
yay -S vmware-workstation
```
### 3.开启服务
```sh
systemctl start vmware-networks.service
systemctl start vmware-usbarbitrator.service
```
### 4.加载VMware模块
```sh
sudo modprobe -a vmw_vmci vmmon
```