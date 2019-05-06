---
layout: post
title:  "c++语言在vs2012环境下利用opc通讯连接组态王"
date:   2019-05-06 14:59:04
categories: c++
tags: c++ 组态王 opc vs2012
---

* content
{:toc}

主要介绍c++语言利用OPC标准库文件与组态王通讯的几个关键步骤，具体代码会在[我的github](https://github.com/neuzhaoxin/c-plus-opc-communication)中贴出来。





## 1、环境配置
将opccomn_ps.dll,PCDAAuto.dll,OpcEnum.exe,opchda_ps.dll,opcproxy.dll这五项全部复制到“C：\Windows\System32”目录下，然后进行注册。

![JPG](pictures/2019-05-06-c++-kingview-opc-communication/20190506151245.jpg)

## 2、核心程序

### 头文件

需要在头文件中包含OPC标准库文件
"Opcda_i.c"，
"Opcda.h"，
"Opccomn_i.c"，
"Opccomn.h"

### 初始化COM库并连接OPC服务器

![JPG](pictures/2019-05-06-c++-kingview-opc-communication/com.jpg)
![JPG](pictures/2019-05-06-c++-kingview-opc-communication/opcserver.jpg)

### 创建OPC组

![JPG](pictures/2019-05-06-c++-kingview-opc-communication/group.jpg)

### 添加Items

![JPG](pictures/2019-05-06-c++-kingview-opc-communication/items.jpg)

### 读取数据
![JPG](pictures/2019-05-06-c++-kingview-opc-communication/read.jpg)

### 写入数据
![JPG](pictures/2019-05-06-c++-kingview-opc-communication/write.jpg)




注：转载请注明，来自https://neuzhaoxin.github.io