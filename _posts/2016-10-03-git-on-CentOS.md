---
layout: post
title: git on CentOS
categories: [git]
tags: [CentOS]
description: CentOS7 安装git
---

在腾讯云上买了一个云服务器，于是便开始了折腾，云服务器作为存储博客内容的远程仓库，为了方便控制，
需要安装git。由于服务器用的CentOS，所以搜索了一下相关内容。

## CentOS7 安装git

1. 查看系统是否已经安装git
```
git --version
```
如果显示的是未找到命令，则表明没有安装。

2. CentOS7 yum 安装git
```
yum install git
```
3. 判断是否安装成功
```
git --version
```
4. 卸载git
```
yum remove git
```

## 从github上把文件pull下来

代码：
```
git remote -v
git remote add origin xxx //(github博客链接)
name:XXX
password:xxx//然后输入名字和密码，密码不会显示，注意不要输错
git remote -v //查看远程仓库
git pull origin master // 下载获取数据
```

### CentOS

CentOS（Community Enterprise Operating System，中文意思是：社区企业操作系统）是Linux
发行版之一，它是来自于Red Hat Enterprise Linux依照开放源代码规定释出的源代码所编译而成。
由于出自同样的源代码，因此有些要求高度稳定性的服务器以CentOS替代商业版的Red Hat
Enterprise Linux使用。两者的不同，在于CentOS并不包含封闭源代码软件。

### yum

Yum（全称为 Yellow dog Updater, Modified）是一个在Fedora和RedHat以及CentOS中的
Shell前端软件包管理器。基于RPM包管理，能够从指定的服务器自动下载RPM包并且安装，
可以自动处理依赖性关系，并且一次安装所有依赖的软件包，无须繁琐地一次次下载、安装。

### SSH

Secure Shell（缩写为SSH），由IETF的网络工作小组（Network Working Group）所制定；
SSH为一项创建在应用层和传输层基础上的安全协议，为计算机上的Shell（壳层）提供安全的传输和使用环境。

传统的网络服务程序，如rsh、FTP、POP和Telnet其本质上都是不安全的；因为它们在网络上用明文传送数据、
用户帐号和用户口令，很容易受到中间人（man-in-the-middle）攻击方式的攻击。
就是存在另一个人或者一台机器冒充真正的服务器接收用户传给服务器的数据，
然后再冒充用户把数据传给真正的服务器。

而SSH是目前较可靠，专为远程登录会话和其他网络服务提供安全性的协议。
利用SSH协议可以有效防止远程管理过程中的信息泄露问题。通过SSH可以对所有传输的数据进行加密，
也能够防止DNS欺骗和IP欺骗。

SSH之另一项优点为其传输的数据可以是经过压缩的，所以可以加快传输的速度。SSH有很多功能，
它既可以代替Telnet，又可以为FTP、POP、甚至为PPP提供一个安全的“通道”。
