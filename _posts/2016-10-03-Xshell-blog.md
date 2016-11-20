---
layout: post
title:Wirting blog by vim
categories: [vim]
tags: [Linux ]
description:Writing blogs using vim
---

### 使用vim编辑器写博客
1. 先打开博客内容所在的文件夹，然后输入vim加上新建文件的名称，即可进入vim编辑器进行编辑。
2. 进入编辑模式需要输入按键a或者i；
3. 如果需要退出按键：ESC；
4. 退出的话按住shift键加冒号，然后就会进入命令行，如果输入wq就是退出；
**注意：所有输入的按键都要在英文输入法中**

### 中文乱码问题

在使用vim的过程中出现了中文乱码问题，解决办法是在进入vi命令行模式后，输入:set encoding=utf-8,发现显示中文正常，那可能是vim本身的问题。
解决办法：
在vi ~/.vimrc 添加set encoding=utf-8 fileencodings=ucs-bom,utf-8,cp936 然后保存，就ok了。
如果在系统中找不到vimrc文件，直接新建一个。
```
vi ~/.vimrc  //新建文件

//然后输入
syntax on

set showmode

set autowrite

set number

set encoding=utf-8 fileencodings=ucs-bom,utf-8,cp936
```
