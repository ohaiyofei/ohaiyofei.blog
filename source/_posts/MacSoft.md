---
layout:     post
title:      MAC系统下日常使用软件的安装
date: 2016/12/31
category: MAC
description: ......
---

## 准备工作
   
首先肯定要保证自己的MACOS系统已经配置好了，具体就是一些在命令行下工作环境的配置，Xcode、安装包管理器Homebrew(类似yum/apt-get)，Zsh、Vim和git的配置，Python环境的管理等等这些工作,具体可参考[这篇博客](http://sourabhbajaj.com/mac-setup/Apps/Settings.html)

## 日常使用

上面配置工作还是挺重要的，我目前也是出于熟悉阶段，不是特别精通，等以后精通了，再来记录一下怎么用MacOS系统搭建舒适的研究开发环境。下面主要介绍一下普通使用者经常需要使用的软件安装：

* [Aria2](https://aria2.github.io/)
* [office2016 for MAC]
* [Matlab2016b for MAC]

下面我来简要总计一下这几个软件安装，第一个是免费开源软件，后面连个是商业软件，这里我使用的是破解版，没钱好吧。。。对于Matla我使用的频率不是特别高了，主要还是用Python/R这些免费开源的软件来代替了，但毕竟用的人挺多的，所以还是在自己电脑装一个吧，以备不时之需。

### Aria2

[Aria2](https://aria2.github.io/)是一款支持多种协议的轻量级命令行下载工具。大家经常需要从网上下载资源（比如百度云盘），但百度云客户端的下载速度实在太慢，所以我主要使用Aria2，这个小软件的优点挺多的，特别跟Chrome的插件配合使用体验非常好。
     
1. 你可以在 [Aria2](https://aria2.github.io/) 的 Download 下载对应的安装程序。下载之后直接双击打开安装即可。  喜欢用homebrew的朋友也可以使用命令' brew install aria2 '来安装
2. 因为Aria2是使用命令行进行下载，但这个还是不太方便，所以要许多人给Aria2开发了许多UI界面,  比如浏览器界面[webui-aria2](https://github.com/ziahamza/webui-aria2)、[Aria2GUI](https://github.com/yangshun1029/aria2gui)等，  我使用的是Aria2GUI，从项目主页下载对应最新版的压缩包，解压缩后，打开dmg文件，然后拖拽Aria2GUI到你的应用文件夹即安装成功，打开运行
3. 根据你使用的浏览器，从[BaiduExporter项目](https://github.com/acgotaku/BaiduExporter)下载浏览器对应的插件并安装连接，  上面有安装教程(之前Chrome的插件商店上，能直接安装的，不知道为啥下架了)，对于Chrome浏览器，还要安装[YAAW](https://github.com/acgotaku/YAAW-for-Chrome),这个可以直接从Chrome商店直接搜索安装。  如果你想从115网盘下载或者迅雷离线，可以下载对应的插件，挺方便的。
4. 启动aria2GUI，重启浏览器，打开你想要下载的百度云盘连接，此时你会看到这个"导出下载“，选择Aria2 RPC. 然后刷新你的Arai2GUI，就可下载相应资源，速度挺快的。

### office2016 for MAC 
配置好了Aria2，安装office2016就很简单，具体步骤如下：

1. 从百度盘下载链接: [https://pan.baidu.com/s/1o8nRXou](https://pan.baidu.com/s/1o8nRXou) 密码: 9y67，下载Office2016 for Mac破解版。
2. 安装完后不要打开office软件，打开破解补丁.dmg，里面有把蓝色的钥匙，双击，出现一把黑色的锁，点击，输入系统密码，OK~搞定

### Matlab2016b for MAC

从百度云盘[https://pan.baidu.com/s/1miQ7RlQ](https://pan.baidu.com/s/1miQ7RlQ) 密码：pha8 下载破解补丁，简单分成三步:
1. 使用Key:09806-07443-53955-64350-21751-41297离线安装Matlab2016b
2. 用破解补丁里libmwservices.dylib替换/Applications/Matlab/bin/maci64/libmwservices.dylib
3. 打开Matlab，使用license.lic离线激活使用，完成
具体可参看这篇[博客](http://www.sdifenzhou.com/matlab2016b.html)

## 总结

最后发现这篇博客主要还是介绍下载工具[Aria2](https://aria2.github.io/)

    

    
     
