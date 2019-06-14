---
layout: post
title:  "win10遇到的一些问题"
date:   2019-05-31 11:24:49
categories: windows 
tags: windows win10
---

* content
{:toc}

记录一下在win10系统下遇到的问题





## 1、虚拟机不兼容(hyper-v和VMware)

我想关闭hyper-v,使用VMware。我的解决方法是借鉴的[这个](https://blog.csdn.net/hotcoffie/article/details/85043894)。

主要利用cmd命令（管理员模式）
```
bcdedit /enum

bcdedit /set {xxxxxxxx} hypervisorlaunchtype off

bcdedit /delete {xxxxxxxxxx}
```
可以将hyper-v完美关闭，之后再用VMware就不会出现不兼容的问题了。





