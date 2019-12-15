---
layout:      post
title:     NFS/NIS环境搭建
date: 2017/7/5
category: note
description: NFS/NIS
---
在nfs的使用过程中，由于server端和client端的帐号不同，可能会造成权限设定上的许多麻烦，通过nis服务统一管理账号则可以解决这个问题,同时通过nfs同步文件目录。

	操作系统：Centos7.2

	NIS服务端：192.168.0.193  node193

	NIS客户端：192.168.0.195  node195
## 准备工作

服务端与客户端hosts文件均有对方主机名与ip映射记录,即在服务端和客户端/etc/hosts文件中编辑添加: 

    192.168.0.193   node193.jasper.com  node193 

    192.168.0.195   node195.jasper.com  mode196

关闭SELinux: 修改/etc/selinux/config，设置SELINUX=disabled，并重启系统，清空防火墙:

    $ iptables -F
	$ iptables -X
    $ iptables -t nat -F
   
## 网络信息服务
NIS主要是实现对主机帐号等系统信息提供集中管理的网络服务，用户登录任何一台NIS客户机都会从NIS服务器进行登录认证，可实现用户帐号的集中管理。在NIS环境中，有三种类型的主机：

* 服务器（master)：充当主机配置信息的中央数据库，保存着用户帐号、 组帐号等配置信息的权威副本
* 从服务器 (slave)：保存这些信息的冗余副本
* 客户机 (client): 使用这些信息

### NIS服务端设置
安装NIS服务端相关软件包：

	$ yum -y install ypserv ypbind yp-tools rpcbind
	
设定NIS的网域名称,NIS是会分domain name来分辨不同的账号密码工具的，因此必须要在服务器端指定NIS域名称，这是指定的域名称为jasper.com :

* 在`/etc/sysconfig/network`中添加域名信息:
	 	
	 	NISDOMAIN=jasper.com
* 设置系统启动时自动设置域名，在`/etc/rc.local`中添加:

		nisdomainname jasper.com


### NIS客户端设置

## 网络文件系统
###  NFS服务端设置
###  NFS客户端设置

     
