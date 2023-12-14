---
title: kde-connect
date: 2023-08-08 17:27:02
tags: KDE
---
# 使用kdeconnect优雅地传文件(局域网)
<!--more-->
### 1.安装
- Windows: [Microsoft Store](https://apps.microsoft.com/store/detail/kde-connect/9N93MRMSXBF0)
- Linux: pkg name is `kdeconnect-kde`, `kdeconnect-plasma`, just `kdeconnect` or `kde-connect`
- Android: [Play Store](https://play.google.com/store/apps/details?id=org.kde.kdeconnect_tp&pli=1)or[F-Droid](https://f-droid.org/packages/org.kde.kdeconnect_tp/)
- IOS: [App Store](https://apps.apple.com/us/app/kde-connect/id1580245991)
### 2.cli
图形界面的使用不再介绍，可以自行探索

使用`kdeconnect-cli -h`查看帮助，获得以下信息
```sh
Usage: kdeconnect-cli [options]
KDE Connect CLI tool

Options:
  -l, --list-devices            List all devices
  -a, --list-available          List available (paired and reachable) devices
  --id-only                     Make --list-devices or --list-available print
                                only the devices id, to ease scripting
  --name-only                   Make --list-devices or --list-available print
                                only the devices name, to ease scripting
  --id-name-only                Make --list-devices or --list-available print
                                only the devices id and name, to ease scripting
  --refresh                     Search for devices in the network and
                                re-establish connections
  --pair                        Request pairing to a said device
  --ring                        Find the said device by ringing it.
  --unpair                      Stop pairing to a said device
  --ping                        Sends a ping to said device
  --ping-msg <message>          Same as ping but you can set the message to
                                display
  --share <path or URL>         Share a file/URL to a said device
  --share-text <text>           Share text to a said device
  --list-notifications          Display the notifications on a said device
  --lock                        Lock the specified device
  --unlock                      Unlock the specified device
  --send-sms <message>          Sends an SMS. Requires destination
  --destination <phone number>  Phone number to send the message
  --attachment <file urls>      File urls to send attachments with the message
                                (can be passed multiple times)
  --device, -d <dev>            Device ID
  --name, -n <name>             Device Name
  --encryption-info             Get encryption info about said device
  --list-commands               Lists remote commands and their ids
  --execute-command <id>        Executes a remote command by id
  -k, --send-keys <key>         Sends keys to a said device
  --my-id                       Display this device's id and exit
  --photo <path>                Open the connected device's camera and transfer
                                the photo
  -h, --help                    Displays help on commandline options.
  --help-all                    Displays help including Qt specific options.
  -v, --version                 Displays version information.
  --author                      Show author information.
  --license                     Show license information.
  --desktopfile <file name>     The base file name of the desktop entry for
                                this application.
```
### 3.使用
```sh
# Arch -> Android
alias kcp="kdeconnect-cli -n <device name> --share"
kcp <path_to_file>
# Android -> Arch
乖乖用GUI罢
```
高级用法请根据自己的习惯和文档自行探索
> 参考链接: https://github.com/KDE/kdeconnect-kde