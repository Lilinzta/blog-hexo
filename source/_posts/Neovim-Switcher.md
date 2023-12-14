---
title: Neovim Switcher
date: 2023-08-15 13:36:46
tags: Neovim
categories: 折腾
---
# 在多种Neovime配置之间无缝切换
<!--more-->
> [视频介绍在这里](https://www.youtube.com/watch?v=LkHjJlSgKZY)

> [不喜欢看视频?](https://gist.github.com/elijahmanor/b279553c0132bfad7eae23e34ceb593b)

zsh用户在.zshrc加入以下配置
```sh
alias nvim-lazy="NVIM_APPNAME=LazyVim nvim"
alias nvim-kick="NVIM_APPNAME=kickstart nvim"
alias nvim-chad="NVIM_APPNAME=NvChad nvim"
alias nvim-astro="NVIM_APPNAME=AstroNvim nvim"

function nvims() {
  items=("default" "kickstart" "LazyVim" "NvChad" "AstroNvim")
  config=$(printf "%s\n" "${items[@]}" | fzf --prompt=" Neovim Config ❯ " --height=~50% --layout=reverse --border --exit-0)
  if [[ -z $config ]]; then
    echo "Nothing selected"
    return 0
  elif [[ $config == "default" ]]; then
    config=""
  fi
  NVIM_APPNAME=$config nvim $@
}

bindkey -s ^a "nvims\n"
```
使用git来管理似乎会很有意思，可惜我git太烂，改天再逝。