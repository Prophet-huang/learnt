# Linux 基础知识

##  Linux操作系统认识，以及开源的提出：Linux的千奇百怪的版本

### 目前世界上流行的电脑系统：

Windows- Bill Gates (比尔·盖茨)
GNU/Linux-Linus Benedict Torvalds(林納斯·托瓦茲)-开源
Unix(Linux的爸爸)- 湯普遜和里奇合-给政府机关、公司等机构付费使用
Linux发行版本：Ubuntu  ，Centos Red ， Hat Kali ……

###  开源的含义

公开、分享、共同进步
开源不一定免费

### Linux的用途，各类发行版本

Linux主要运用在服务器上

Linux严格来说是单指操作**系统的内核**，因操作系统中包含了许多用户图形接口和其他实用工具
只要遵循GNU 通用公共许可证（GPL），任何个人和机构都可以自由地使用Linux的所有底层源代码，也可以自由地修改和再发布

#### Linux衍生（发行版本）：

Debian —> 代表的系统名：Ubuntu	,Deepin	,Raspberry Pi OS	,Knopix
Fedora —> 代表的系统名：RedHat	,Centos	,Moblin
OpenSUSE —>代表的系统名： GeckoLinux	,openSUSE  ,EcoLab Spin



其实Android，也是 LInux 的内核，通过小工具操作也可以变成，既可体验。

国产的手机考虑到所谓安全问题，不开放。

------



#  Linux究竟需要我们学习什么？——Linux四大组成部分

Linux入门不是学“Linux”，先体验各发行版Linux，比较和其他系统的不同和相同点，Linux究竟学习的是Shell

### Linux操作系统四个部分

Linux Kernel 内核
GNU(“GNU’s Not Unix!”)工具
GUI Desktop环境
Application 应用
PS：IT术语，它并不是遵循通常的英语音标，而是专业术语

## Linux是命令还是图形界面？——GUI 是什么？ 那GNU是什么东西？GNU/Linux 和Linux有什么区别？

### Linux内核的基于：

GUI-界面
GNU-命令、系统工具

#### Linux Kernel（Linux内核） 组成部分

1.硬件设备的管理
2.软件程序(系统)、操作软件
3.系统内存
4.文件管理

##### 文件系统

文件系统就是读、写标准

###### 文件系统的分区的格式

Linux中分区概念ext ext2 ext3 ext4
Windows 磁盘文件管理概念FAT32 NTFS exFAT

### GNU核心： coreutils（核心工具组） and shell（shell命令）

#### GNU是一个组织

Unix上具有的一些软件，Linux内核本身没有，所以GNU他们模仿Unix，为Linux写了一些必要的软件

#### GNU核心Coreutils

指原本在Unix上的一些命令和工具，被移植到了Linux上，供Linux使用的一套工具、coreutilities软件包，包括:

用来处理文件的工具
用来操作文本的工具
用来管理进程的工具

#### GNU核心Shell

提供给用户使用的软件，用户拿它使用电脑，实现交互

Shell 有两种：CLI（命令）和GUI（界面）

命令行壳层提供一个命令行界面（CLI），在计算机专业中大多数情况下这 shell 指的就是他。

图像壳层提供一个图形用户界面（GUI）

##### Shell CLI（命令）类型：

bash，zsh，korn，tcsh，oh-my-zsh


##### Shell GUI （界面）类型：

Xwindows，KDE，GNOME，Unity

