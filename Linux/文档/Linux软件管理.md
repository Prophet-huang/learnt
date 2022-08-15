# PMS(package management system)

包管理系统

工具依赖：某些软件需要依赖其他软件工具运行，由于安装过程繁琐，因此出现了PMS来简化软件的安装。

许多Linux发行版本都有包管理软件，类似手机应用商店，包管理软件可以满足人们对软件安装、更新以及卸载的所有要求。简化了软件的安装、更新和卸载。软件开发者准许规范将程序编译、打包，并上传到公开的服务器中，供系统用户通过包管理工具获取。

**`dpkg`(Debian Packager):**

是Debian开发的底层包管理工具，是包管理系统的基础。`dpkg`用于安装、卸载以及升级，但是使用`dpkg`需要提供 .deb软件包，也就是说`dpkg`仅仅是本地安装，需要开发者提供资源，所以使用`dpkg`安装会存在一个问题就是，开发者需要自行解决依赖问题。



------

# APT 软件的安装、更新、卸载

Debian Linux发行版中的APT软件包管理工具

是Debian Linux发行版中的APT软件包管理工具。所有基于Debian的发行都使用这个包管理系统。deb包可以把一个应用的文件包在一起，大体就如同Windows上的安装文件。

**注意：不同发行版本的Linux上，安装命令可能不一致。**
如：CentOS上安装命令为yum install …

## 语法

```bash
apt [OPTION] PACKAGE     #新版Linux可以取消-get
apt-get [OPTION] PACKAGE #旧版必须要有
```



## 选项

```bash
apt-get install  # 安装新包
apt-get remove   # 卸载已安装的包（保留配置文件）
apt-get purge    # 卸载已安装的包（删除配置文件）
apt-get update   # 更新软件包列表
apt-get upgrade  # 升级所有已安装的包
apt-get autoremove   # 卸载已不需要的包依赖
apt-get dist-upgrade # 自动处理依赖包升级
apt-get autoclean    # 将已经删除了的软件包的.deb安装文件从硬盘中删除掉
apt-get clean        # 删除软件包的安装包

-c：指定配置文件。
```





```bash
apt-get upgrade  # 升级所有已安装的包
# 关于升级包时可能出现的异常：
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 1924 
翻译：等待缓存锁定：无法获取锁定 /var/lib/dpkg/lock-frontend。它由过程1924持有
'/var/lib/dpkg/lock-frontend' 文件被 进程 1924 占用了，此步骤的操作原因是多次使用apt -y install 安装某软件导致的请求频繁，进程ps出现多次/卡顿延迟，所以才执行。

解决方案：
1.删除锁定文件：rm -f /var/lib/dpkg/lock/*
2.强制干掉进程：kill -9 1924

```



------



# 安装软件时要留意的一些问题

## 下载慢

在国内下载慢要考虑，镜像源是否配置好。

`Ubuntu`配置镜像源的文件在：

```bash
/etc/apt/source.list
```

 **记得管理员命令修改**

`Ubuntu`镜像源地址与阿里镜像源地址参考：

```bash
http://archive.ubuntu.com/ubuntu/
http://mirrors.aliyun.com/ubuntu/
```

**实际更换流程去网上查，每个版本都有差异，但如果要修改文件，请现将源文件备份。**

------



## 安装第三方软件推荐流程

1. 以一定要读安装须知：`README.md` 文件。
2. 查看安装该软件有什么要求（Requirements）：依赖什么其他工具或者支持的版本号。
3. 查看看装与自己系统适配的安装方法。
4. 安装后别忘配置环境变量。
5. 查看更新方式和写在方式。