---
Status: Finished
Title: Java环境搭建
Index: 4
---
# Java环境搭建
# No.1-导读

欢迎阅读Java环境搭建，在开始之前，请注意本指南适用于任何初学者的配置JDK。

本教程主要通过JDK11进行搭建，并基于破碎的像素地牢1.2.3进行配置。

注意：如果您使用的是2.1.0以上的破碎地牢版本，JDK11将无法胜任编译工作。这是源于Evan(破碎地牢作者)在2.1.0进行了Gradle版本迭代，它的Gradle Build Tools 为8.0.0，此构建版本无法支持JDK11,需要使用JDK17才能进行编译运行。但本系列指南主要通过1.2.3破碎进行引导，所以请非特殊情况，不要使用1.2.3之外的版本。

本教程主要针对于JDK11进行配置说明，全文进行图文流程，方便各位迅速配置好JDK11。

破碎的像素地牢底层版本JDK支持列表：

0.1.X-0.9.X  最低支持：JDK8

1.0.X-1.4.X  最低支持：JDK11

2.0.X-2.1.X  最低支持：JDK17

# No.2-配置

## 1.下载JDK:

JDK11下载路径（推荐微软的下载地址）：

[https://learn.microsoft.com/zh-cn/java/openjdk/download#openjdk-11](https://learn.microsoft.com/zh-cn/java/openjdk/download#openjdk-11)

JDK17下载路径（推荐微软的下载地址）：

[https://learn.microsoft.com/zh-cn/java/openjdk/download#openjdk-17](https://learn.microsoft.com/zh-cn/java/openjdk/download#openjdk-17)

## 2.选择下载版本

然后根据下图下载需要的版本：

注意：如果你是Linux系统开发地牢，你应该百度Linux如何安装JDK。

且Linux属于服务器操作系统，玩这种系统的通常也有一定的IT知识，对此我们并不展开Linux安装JDK的讨论。

![[Pasted image 20230816134154.png]]
## 3.安装MSI

下载完成后，打开对应的MSI(Microsoft Install)安装包，双击运行，路径不要乱改，默认即可。

注意：除非你已经知晓JDK配置，否则请不要修改JDK路径。（记住JDK路径）

## 4.配置环境变量

### A.  先找到自己的此电脑，并点击属性

![[Pasted image 20230816134113.png]]
### B.  高级系统设置

![[Pasted image 20230816134116.png]]
### C.  寻找环境变量

![[Pasted image 20230816134118.png]]
### D.  配置系统变量

![[Pasted image 20230816134120.png]]
### E.  配置JDK环境变量系列步骤

新建一个叫JAVA_HOME的属性，路径使用你刚才安装的JDK的根目录：

JDK17默认路径参考：
```plain
C:\Program Files\Microsoft\jdk-17.0.7.7-hotspot
```

![[Pasted image 20230816134122.png]]

新建/修改 一个叫CLASSPATH的属性：

![[Pasted image 20230816134124.png]]

输入以下内容：

变量名：
```plain
CLASSPATH  
```

变量值：
```plain
.;%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar;
```

![[Pasted image 20230816134126.png]]
新建/修改Path属性：
![[Pasted image 20230816134129.png]]

在用户变量的Path中新建两行，输入以下内容：
```plain
%JAVA_HOME%\bin
```
```plain
%JAVA_HOME%\jre\bin
```

![[Pasted image 20230816134131.png]]

![[Pasted image 20230816134133.png]]
### F.  核查JDK是否配置成功

Win+R呼出运行对话框，输入cmd，回车Enter后。

键入以下命令验证JDK11是否安装成功：

```plain
java
```
```plain
java -version
```

若均有cmd消息反馈，且显示不为'java'不是内部或外部命令，也不是可运行的程序，或批处理文件。即为配置成功。配置成功的截图如下图所示。

PS:如果你配置失败，请仔细筛查你的步骤是否与教程有遗漏。

![[Pasted image 20230816134136.png]]

配置成功的样例截图：

![[Pasted image 20230816134154.png]]

# No.3-结语和后续步骤

至此，JDK配置就告一段落了。当然，这只是一个开始。接下来你将接触你今后频繁使用的一个软件“Android Stuido”，有关于AS的配置教程，请移步下一教程。