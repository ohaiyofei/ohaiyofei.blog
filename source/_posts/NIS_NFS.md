---
layout:      post
title:     NFS/NIS环境搭建
date: 2017/7/5
category: note
description: NFS/NIS
---
在nfs的使用过程中，由于server端和client端的帐号不同，可能会造成权限设定上的许多麻烦，通过nis服务统一管理账号则可以解决这个问题,同时通过nfs同步文件目录。
####操作系统：Centos7.2

####NIS服务端：192.168.0.193  node193

####NIS客户端：192.168.0.195  node195
## 准备工作

服务端与客户端hosts文件均有对方主机名与ip映射记录,即在服务端和客户端/etc/hosts文件中编辑添加: 

192.168.0.193  node193.jasper.com  node193 

192.168.0.195  node195.jasper.com  mode196

关闭SELinux: 修改/etc/selinux/config，设置SELINUX=disabled，并重启系统，清空防火墙

   * iptables -F
   * iptables -X
   * iptables -t nat -F
   
##网络信息服务

### NIS服务端设置
### NIS客户端设置

##网络文件系统
###  NFS服务端设置
###  NFS客户端设置

     
