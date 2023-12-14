---
title: Arch Linux切换java环境
date: 2023-10-23 17:06:06
tags: Arch Linux
categories: 技巧
---
### archlinux-java
输出如下:
```sh
❯ archlinux-java --help
archlinux-java <COMMAND>

COMMAND:
	status		List installed Java environments and enabled one
	get		Return the short name of the Java environment set as default
	set <JAVA_ENV>	Force <JAVA_ENV> as default
	unset		Unset current default Java environment
	fix		Fix an invalid/broken default Java environment configuration
```
### Examples
获取当前设置:
```sh
❯ archlinux-java get
java-21-openjdk
```
查看所有可用Java环境
```sh
❯ archlinux-java status
Available Java environments:
  java-11-openjdk
  java-17-openjdk
  java-21-openjdk (default)
  java-8-openjdk
```
要更改默认设置，请使用root权限:
```sh
❯ sudo archlinux-java set java-17-openjdk
```