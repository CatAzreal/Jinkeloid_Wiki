---
Status: Undone
Title: Android Studio安装
Index: 5
---
# Android Studio安装

# No.1-导读

如果想要完全按照本指南安装必要软件，==**请不要为安装的任何软件自定义路径，同时请确保所有安装文件都位于英文路径下，对于初学者来说，任何不遵守指南的操作都可能导致最终结果与指南不符。**==

本页指南将向读者展示Android Studio的安装。

如前言所述，为了保证流程的标准化，本页指南将展示2022.2.1.20版本的安装，同时建议跟随本指南的读者严格按照流程操作。

# No.2-配置

## 1.下载

[Android Studio2022.2.1.20下载地址](https://redirector.gvt1.com/edgedl/android/studio/install/2022.2.1.20/android-studio-2022.2.1.20-windows.exe)

## 2.安装

下图的Android Virtual Device为自带虚拟机，电脑性能和内存均足够的情况下可以勾选，后续调试应用相对会方便一点。
![[Pasted image 20230824170629.png]]

## 3.启动

忽略导入配置窗口，直接点击ok。
![[Pasted image 20230824170733.png]]

进入Android Studio Setup Wizard，在没有vpn和代理的情况下，稍待片刻就会弹出窗口报错，取消，然后继续安装流程。 
![[Pasted image 20230824174639.png]]

继续SDK的下载与安装，选择Standard，执行标准化安装：
![[Pasted image 20230824171642.png]]

同意安装证书，然后完成SDK安装确认：
![[Pasted image 20230824171847.png]]

等待下载完成，需要花费一点时间：
![[Pasted image 20230824174745.png]]

# No.3-结语

Android Studio的安装到这里就结束了，接下来我们需要安装git，并在此之后导入破碎源码。关于Git安装，请移步至[[103-Git安装]]；关于导入源码，请移步至[[201-项目导入]]。