# Linux

## 简介

Linux 是一种自由和开放源码的类 UNIX 操作系统，使用 Linux 内核。目前存在着许多不同的 Linux 发行版，可安装在各种各样的电脑硬件设备，从手机、平板电脑、路由器和影音游戏控制台，到桌上型电脑，大型电脑和超级电脑。 Linux 是一个领先的操作系统，世界上运算最快的 10 台超级电脑运行的都是 Linux 操作系统。

Linux 操作系统也是自由软件和开放源代码发展中最著名的例子。只要遵循 GNU 通用公共许可证,任何人和机构都可以自由地使用 Linux 的所有底层源代码，也可以自由地修改和再发布。严格来讲，Linux 这个词本身只表示 Linux 内核，但在实际上人们已经习惯了用 Linux 来形容整个基于 Linux 内核，并且使用 GNU 工程各种工具和数据库的操作系统 (也被称为 GNU/ Linux)。通常情况下，Linux 被打包成供桌上型电脑和服务器使用的 Linux 发行版本。一些流行的主流 Linux 发行版本，包括 Debian (及其衍生版本 Ubuntu)，Fedora 和 OpenSUSE 等。Kernel + Softwares + Tools 就是 Linux Distribution

目前市面上较知名的发行版有：`Ubuntu`、RedHat、`CentOS`、Debian、Fedora、SuSE、OpenSUSE、TurboLinux、BluePoint、RedFlag、Xterm、SlackWare等。

## Linux 与 Windows 比较

目前国内 Linux 更多的是应用于服务器上，而桌面操作系统更多使用的是 Windows。主要区别如下

| 比较   | Windows                                  | Linux                                    |
| ---- | ---------------------------------------- | ---------------------------------------- |
| 界面   | 界面统一，外壳程序固定所有 Windows 程序菜单几乎一致，快捷键也几乎相同  | 图形界面风格依发布版不同而不同，可能互不兼容。GNU/Linux 的终端机是从 UNIX 传承下来，基本命令和操作方法也几乎一致。 |
| 驱动程序 | 驱动程序丰富，版本更新频繁。默认安装程序里面一般包含有该版本发布时流行的硬件驱动程序，之后所出的新硬件驱动依赖于硬件厂商提供。对于一些老硬件，如果没有了原配的驱动有时很难支持。另外，有时硬件厂商未提供所需版本的 Windows 下的驱动，也会比较头痛。 | 由志愿者开发，由Linux核心开发小组发布，很多硬件厂商基于版权考虑并未提供驱动程序，尽管多数无需手动安装，但是涉及安装则相对复杂，使得新用户面对驱动程序问题（是否存在和安装方法）会一筹莫展。但是在开源开发模式下，许多老硬件尽管在 Windows 下很难支持的也容易找到驱动。HP、Intel、AMD 等硬件厂商逐步不同程度支持开源驱动，问题正在得到缓解。 |
| 使用   | 使用比较简单，容易入门。图形化界面对没有计算机背景知识的用户使用十分有利。    | 图形界面使用简单，容易入门。文字界面，需要学习才能掌握。             |
| 学习   | 系统构造复杂、变化频繁，且知识、技能淘汰快，深入学习困难。            | 系统构造简单、稳定，且知识、技能传承性好，深入学习相对容易。           |
| 软件   | 每一种特定功能可能都需要商业软件的支持，需要购买相应的授权。           | 大部分软件都可以自由获取，同样功能的软件选择较少。                |

## 安装 Ubuntu Server

原生云应用基本都是基于云服务器部署，本地化的 Linux 操作基本也都是在虚拟机中进行模拟操作。故我们只需要安装虚拟机并在虚拟机上安装对应的 Linux 操作系统即可。

## 安装 VMware

不提供具体的安装说明，请自行查阅相关资料

## 安装 Ubuntu Server

具体安装过程请看视频：https://www.bilibili.com/video/av27095828/

## Linux 远程控制管理

### 概述

传统的网络服务程序，FTP、POP、telnet 本质上都是不安全的，因为它们在网络上通过明文传送口令和数据，这些数据非常容易被截获。SSH 叫做 `Secure Shell`。通过 SSH，可以把传输数据进行加密，预防攻击，传输的数据进行了压缩，可以加快传输速度。

### OpenSSH

SSH 是芬兰一家公司开发。但是受到版权和加密算法限制，现在很多人都使用 OpenSSH。OpenSSH 是 SSH 的替代软件，免费。

OpenSSH 由客户端和服务端组成。

- 基于口令的安全验证：知道服务器的帐号密码即可远程登录，口令和数据在传输过程中都会被加密。
- 基于密钥的安全验证：此时需要在创建一对密钥，把公有密钥放到远程服务器上自己的宿主目录中，而私有密钥则由自己保存。

### 检查软件是否安装

```
apt-cache policy openssh-client openssh-server

```

### 安装服务端

```
apt-get install openssh-server

```

### 安装客户端

```
apt-get install openssh-client

```

OpenSSH 服务器的主要配置文件为 `/etc/ssh/sshd\_config`，几乎所有的配置信息都在此文件中。

### XShell

XShell 是一个强大的安全终端模拟软件，它支持 SSH1, SSH2, 以及 Microsoft Windows 平台的 TELNET 协议。XShell 通过互联网到远程主机的安全连接以及它创新性的设计和特色帮助用户在复杂的网络环境中享受他们的工作。

XShell 可以在 Windows 界面下用来访问远端不同系统下的服务器，从而比较好的达到远程控制终端的目的。

效果图如下：

![](/Linux-img/001.png)

## Linux 目录结构

![](/Linux-img/002.png)

| 目录   | 说明                                       |
| ---- | ---------------------------------------- |
| bin  | 存放二进制可执行文件(ls,cat,mkdir等)                |
| boot | 存放用于系统引导时使用的各种文件                         |
| dev  | 用于存放设备文件                                 |
| etc  | 存放系统配置文件                                 |
| home | 存放所有用户文件的根目录                             |
| lib  | 存放跟文件系统中的程序运行所需要的共享库及内核模块                |
| mnt  | 系统管理员安装临时文件系统的安装点                        |
| opt  | 额外安装的可选应用程序包所放置的位置                       |
| proc | 虚拟文件系统，存放当前内存的映射                         |
| root | 超级用户目录                                   |
| sbin | 存放二进制可执行文件，只有root才能访问                    |
| tmp  | 用于存放各种临时文件                               |
| usr  | 用于存放系统应用程序，比较重要的目录/usr/local 本地管理员软件安装目录 |
| var  | 用于存放运行时需要改变数据的文件                         |

## Linux 操作文件目录

| 命令    | 说明                | 语法                                       | 参数    | 参数说明              |
| ----- | ----------------- | ---------------------------------------- | ----- | ----------------- |
| ls    | 显示文件和目录列表         | ls [-alrtAFR] [name...]                  |       |                   |
|       |                   |                                          | -l    | 列出文件的详细信息         |
|       |                   |                                          | -a    | 列出当前目录所有文件，包含隐藏文件 |
| mkdir | 创建目录              | mkdir [-p] dirName                       |       |                   |
|       |                   |                                          | -p    | 父目录不存在情况下先生成父目录   |
| cd    | 切换目录              | cd [dirName]                             |       |                   |
| touch | 生成一个空文件           |                                          |       |                   |
| echo  | 生成一个带内容文件         | echo abcd > 1.txt，echo 1234 >> 1.txt     |       |                   |
| cat   | 显示文本文件内容          | cat [-AbeEnstTuv] [--help] [--version] fileName |       |                   |
| cp    | 复制文件或目录           | cp [options] source dest                 |       |                   |
| rm    | 删除文件              | rm [options] name...                     |       |                   |
|       |                   |                                          | -f    | 强制删除文件或目录         |
|       |                   |                                          | -r    | 同时删除该目录下的所有文件     |
| mv    | 移动文件或目录           | mv [options] source dest                 |       |                   |
| find  | 在文件系统中查找指定的文件     |                                          |       |                   |
|       |                   |                                          | -name | 文件名               |
| grep  | 在指定的文本文件中查找指定的字符串 |                                          |       |                   |
| tree  | 用于以树状图列出目录的内容     |                                          |       |                   |
| pwd   | 显示当前工作目录          |                                          |       |                   |
| ln    | 建立软链接             |                                          |       |                   |
| more  | 分页显示文本文件内容        |                                          |       |                   |
| head  | 显示文件开头内容          |                                          |       |                   |
| tail  | 显示文件结尾内容          |                                          |       |                   |
|       |                   |                                          | -f    | 跟踪输出              |

## Linux 系统管理目录

| 命令       | 说明                      |
| -------- | ----------------------- |
| stat     | 显示指定文件的相关信息,比ls命令显示内容更多 |
| who      | 显示在线登录用户                |
| hostname | 显示主机名称                  |
| uname    | 显示系统信息                  |
| top      | 显示当前系统中耗费资源最多的进程        |
| ps       | 显示瞬间的进程状态               |
| du       | 显示指定的文件（目录）已使用的磁盘空间的总量  |
| df       | 显示文件系统磁盘空间的使用情况         |
| free     | 显示当前内存和交换空间的使用情况        |
| ifconfig | 显示网络接口信息                |
| ping     | 测试网络的连通性                |
| netstat  | 显示网络状态信息                |
| clear    | 清屏                      |
| kill     | 杀死一个进程                  |

## Linux 开关机命令

shutdown 命令可以用来进行关机程序，并且在关机以前传送讯息给所有使用者正在执行的程序，shutdown 也可以用来重开机。

| 命令       | 语法                                       | 参数         | 参数说明                             |
| -------- | ---------------------------------------- | ---------- | -------------------------------- |
| shutdown | shutdown [-t seconds] [-rkhncfF] time [message] |            |                                  |
|          |                                          | -t seconds | 设定在几秒钟之后进行关机程序                   |
|          |                                          | -k         | 并不会真的关机，只是将警告讯息传送给所有只用者          |
|          |                                          | -r         | 关机后重新开机（重启）                      |
|          |                                          | -h         | 关机后停机                            |
|          |                                          | -n         | 不采用正常程序来关机，用强迫的方式杀掉所有执行中的程序后自行关机 |
|          |                                          | -c         | 取消目前已经进行中的关机动作                   |
|          |                                          | -f         | 关机时，不做 fcsk 动作(检查 Linux 档系统)     |
|          |                                          | -F         | 关机时，强迫进行 fsck 动作                 |
|          |                                          | time       | 设定关机的时间                          |
|          |                                          | message    | 传送给所有使用者的警告讯息                    |

### 重启

- reboot
- shutdown -r now

### 关机

- shutdown -h now

## Linux 压缩命令

### tar

| 命令   | 语法                            | 参数   | 参数说明              |
| ---- | ----------------------------- | ---- | ----------------- |
| tar  | tar [-cxzjvf] 压缩打包文档的名称 欲打包目录 |      |                   |
|      |                               | -c   | 建立一个归档文件的参数指令     |
|      |                               | -x   | 解开一个归档文件的参数指令     |
|      |                               | -z   | 是否需要用 gzip 压缩     |
|      |                               | -j   | 是否需要用 bzip2 压缩    |
|      |                               | -v   | 压缩的过程中显示文件        |
|      |                               | -f   | 使用档名，在 f 之后要立即接档名 |
|      |                               | -tf  | 查看归档文件里面的文件       |

**例子：**

- 压缩文件夹：`tar -zcvf test.tar.gz test\`
- 解压文件夹：`tar -zxvf test.tar.gz`

### gzip

| 命令   | 语法                    | 参数   | 参数说明                                     |
| ---- | --------------------- | ---- | ---------------------------------------- |
| gzip | gzip [选项] 压缩（解压缩）的文件名 |      |                                          |
|      |                       | -d   | 解压缩                                      |
|      |                       | -l   | 对每个压缩文件，显示压缩文件的大小，未压缩文件的大小，压缩比，未压缩文件的名字  |
|      |                       | -v   | 对每一个压缩和解压的文件，显示文件名和压缩比                   |
|      |                       | -num | 用指定的数字num调整压缩的速度，-1或--fast表示最快压缩方法（低压缩比），-9或--best表示最慢压缩方法（高压缩比）。系统缺省值为6 |

说明：压缩文件后缀为 gz

### bzip2

| 命令    | 语法           | 参数   | 参数说明                                     |
| ----- | ------------ | ---- | ---------------------------------------- |
| bzip2 | bzip2 [-cdz] |      |                                          |
|       |              | -d   | 解压缩                                      |
|       |              | -z   | 压缩参数                                     |
|       |              | -num | 用指定的数字num调整压缩的速度，-1或--fast表示最快压缩方法（低压缩比），-9或--best表示最慢压缩方法（高压缩比）。系统缺省值为6 |

说明：压缩文件后缀为 bz2

## Linux 编辑器

### vim

#### 运行模式

编辑模式：等待编辑命令输入

插入模式：编辑模式下，输入 `i` 进入插入模式，插入文本信息

命令模式：在编辑模式下，输入 `:` 进行命令模式

#### 命令

`:q` 直接退出vi

`:wq` 保存后退出vi ，并可以新建文件

`:q!` 强制退出

`:w file` 将当前内容保存成某个文件

`:set number` 在编辑文件显示行号

`:set nonumber`	在编辑文件不显示行号

### nano

nano 是一个字符终端的文本编辑器，有点像 DOS 下的 editor 程序。它比 vi/vim 要简单得多，比较适合 Linux 初学者使用。某些 Linux 发行版的默认编辑器就是 nano。

#### 命令

- 保存：ctrl + o
- 搜索：ctrl + w
- 上一页：ctrl + y
- 下一页：ctrl + v
- 退出：ctrl + x

## Linux 软件包管理

APT(Advanced Packaging Tool) 是 Debian/Ubuntu 类 Linux 系统中的软件包管理程序, 使用它可以找到想要的软件包, 而且安装、卸载、更新都很简便；也可以用来对 Ubuntu 进行升级; APT 的源文件为 `/etc/apt/` 目录下的 `sources.list` 文件。

### 修改数据源

由于国内的网络环境问题，我们需要将 Ubuntu 的数据源修改为国内数据源，操作步骤如下：

### 查看系统版本

```sh
lsb_release -a
```

输出结果为

```sh
No LSB modules are available.
Distributor ID:	Ubuntu
Description:	Ubuntu 16.04 LTS
Release:	16.04
Codename:	xenial
```

**注意：** Codename 为 `xenial`，该名称为我们 Ubuntu 系统的名称，修改数据源需要用到该名称

### 编辑数据源

```sh
vi /etc/apt/sources.list
```

删除全部内容并修改为

```sh
deb http://mirrors.aliyun.com/ubuntu/ xenial main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse
```

### 更新数据源

```sh
apt-get update
```

## 常用 APT 命令

### 安装软件包

```sh
apt-get install packagename
```

### 删除软件包

```sh
apt-get remove packagename
```

### 更新软件包列表

```sh
apt-get update
```

### 升级有可用更新的系统（慎用）

```sh
apt-get upgrade
```

## 其它 APT 命令

### 搜索

```sh
apt-cache search package
```

### 获取包信息

```
apt-cache show package
```

### 删除包及配置文件

```
apt-get remove package --purge
```

### 了解使用依赖

```
apt-cache depends package
```

### 查看被哪些包依赖

```
apt-cache rdepends package
```

### 安装相关的编译环境

```
apt-get build-dep package
```

### 下载源代码

```
apt-get source package
```

### 清理无用的包

```
apt-get clean && apt-get autoclean
```

### 检查是否有损坏的依赖

```
apt-get check
```

## Linux 用户和组管理

Linux 操作系统是一个多用户操作系统，它允许多用户同时登录到系统上并使用资源。系统会根据账户来区分每个用户的文件，进程，任务和工作环境，使得每个用户工作都不受干扰。

### 使用 Root 用户

在实际生产操作中，我们基本上都是使用超级管理员账户操作 Linux 系统，也就是 Root 用户，Linux 系统默认是关闭 Root 账户的，我们需要为 Root 用户设置一个初始密码以方便我们使用。

#### 设置 Root 账户密码

```
sudo passwd root
```

#### 切换到 Root

```
su
```

#### 设置允许远程登录 Root

```
nano /etc/ssh/sshd_config

# Authentication:
LoginGraceTime 120
#PermitRootLogin without-password     //注释此行
PermitRootLogin yes                             //加入此行
StrictModes yes

重启服务
service ssh restart
```

### 用户账户说明

#### 普通用户

普通用户在系统上的任务是进行普通操作

#### 超级管理员

管理员在系统上的任务是对普通用户和整个系统进行管理。对系统具有绝对的控制权，能够对系统进行一切操作。用 root 表示，root 用户在系统中拥有最高权限，默认下 Ubuntu 用户的 root 用户是不能登录的。

#### 安装时创建的系统用户

此用户创建时被添加到 admin 组中，在 Ubuntu 中，admin 组中的用户默认是可以使用 `sudo` 命令来执行只有管理员才能执行的命令的。如果不使用 `sudo` 就是一个普通用户。

#### 组账户说明

##### 私有组

当创建一个用户时没有指定属于哪个组，Linux 就会建立一个与用户同名的私有组，此私有组只含有该用户。

##### 标准组

当创建一个用户时可以选定一个标准组，如果一个用户同时属于多个组时，登录后所属的组为主组，其他的为附加组。

### 账户系统文件说明

#### /etc/passwd

每一行代表一个账号，众多账号是系统正常运行所必须的，例如 bin，nobody 每行定义一个用户账户，此文件对所有用户可读。每行账户包含如下信息：

`root:x:0:0:root:/root:/bin/bash`

- **用户名：** 就是账号，用来对应 UID，root UID 是 0。
- **口令：** 密码，早期 UNIX 系统密码存在此字段，由于此文件所有用户都可以读取，密码容易泄露，后来这个字段数据就存放到 /etc/shadow 中，这里只能看到 X。
- **用户标示号（UID）：** 系统内唯一，root 用户的 UID 为 0，普通用户从 1000 开始，1-999 是系统的标准账户，500-65536 是可登陆账号。
- **组标示号（GID）：** 与 /etc/group 相关用来规定组名和 GID 相对应。
- **注释：** 注释账号
- **宿主目录（主文件夹）：** 用户登录系统后所进入的目录 root 在 /root/itcast
- **命令解释器（shell）：** 指定该用户使用的 shell ，默认的是 /bin/bash

#### /etc/shadow

为了增加系统的安全性，用户口令通常用 shadow passwords 保护。只有 root 可读。每行包含如下信息：

`root:$6$Reu571.V$Ci/kd.OTzaSGU.TagZ5KjYx2MLzQv2IkZ24E1.yeTT3Pp4o/yniTjus/rRaJ92Z18MVy6suf1W5uxxurqssel.:17465:0:99999:7:::`

- **账号名称：** 需要和 /etc/passwd 一致。

- 密码：

   

  经过加密，虽然加密，但不表示不会被破解，该文件默认权限如下：

  - -rw------- 1 root root 1560 Oct 26 17:20 passwd-
  - 只有root能都读写

- **最近修改密码日期：** 从1970-1-1起，到用户最后一次更改口令的天数

- **密码最小时间间隔：** 从1970-1-1起，到用户可以更改口令的天数

- **密码最大时间间隔：** 从1970-1-1起，必须更改的口令天数

- **密码到期警告时间：** 在口令过期之前几天通知

- **密码到期后账号宽限时间**

- **密码到期禁用账户时间：** 在用户口令过期后到禁用账户的天数

- **保留**

#### /etc/group

用户组的配置文件

`root:x:0:`

- **用户组名称**
- **用户组密码：** 给用户组管理员使用，通常不用
- **GID：** 用户组的ID
- **此用户支持的账号名称：** 一个账号可以加入多个用户组，例如想要 itcast 加入 root 这个用户组，将该账号填入该字段即可 root❌0:root, icast 将用户进行分组是 Linux 对用户进行管理及控制访问权限的一种手段。一个中可以有多个用户，一个用户可以同时属于多个组。该文件对所有用户可读。

#### /etc/gshadow

该文件用户定义用户组口令，组管理员等信息只有root用户可读。

`root:\*::`

- **用户组名**
- **密码列**
- **用户组管理员的账号**
- **用户组所属账号**

### 账户管理常用命令

#### 增加用户

```
useradd 用户名
useradd -u (UID号)
useradd -p (口令)
useradd -g (分组)
useradd -s (SHELL)
useradd -d (用户目录)
```

如：`useradd lusifer`

增加用户名为 lusifer 的账户

#### 修改用户

```
usermod -u (新UID)
usermod -d (用户目录)
usermod -g (组名)
usermod -s (SHELL)
usermod -p (新口令)
usermod -l (新登录名)
usermod -L (锁定用户账号密码)
usermod -U (解锁用户账号)
```

如：`usermod -u 1024 -g group2 -G root lusifer`

将 lusifer 用户 uid 修改为 1024，默认组改为系统中已经存在的 group2，并且加入到系统管理员组

#### 删除用户

```
userdel 用户名 (删除用户账号)
userdel -r 删除账号时同时删除目录
```

如：`userdel -r lusifer`

删除用户名为 lusifer 的账户并同时删除 lusifer 的用户目录

#### 组账户维护

```
groupadd 组账户名 (创建新组)
groupadd -g 指定组GID
groupmod -g 更改组的GID
groupmod -n 更改组账户名
groupdel 组账户名 (删除指定组账户)
```



#### 口令维护

```
passwd 用户账户名 (设置用户口令)
passwd -l 用户账户名 (锁定用户账户)
passwd -u 用户账户名 (解锁用户账户)
passwd -d 用户账户名 (删除账户口令)
gpasswd -a 用户账户名 组账户名 (将指定用户添加到指定组)
gpasswd -d 用户账户名 组账户名 (将用户从指定组中删除)
gpasswd -A 用户账户名 组账户名 (将用户指定为组的管理员)
```

#### 用户和组状态

```
su 用户名(切换用户账户)
id 用户名(显示用户的UID，GID)
whoami (显示当前用户名称)
groups (显示用户所属组)
```

## Linux 文件权限管理

### 查看文件和目录的权限

ls –al`使用 ls 不带参数只显示文件名称，通过`ls –al` 可以显示文件或者目录的权限信息。

`ls -l 文件名` 显示信息包括：文件类型 (`d` 目录，`-` 普通文件，`l` 链接文件)，文件权限，文件的用户，文件的所属组，文件的大小，文件的创建时间，文件的名称

`-rw-r--r-- 1 lusifer lusifer 675 Oct 26 17:20 .profile`

- `-`：普通文件
- `rw-`：说明用户 lusifer 有读写权限，没有运行权限
- `r--`：表示用户组 lusifer 只有读权限，没有写和运行的权限
- `r--`：其他用户只有读权限，没有写权限和运行的权限

| -rw-r--r-- | 1    | lusifer | lusifer | 675  | Oct 26 17:20 | .profile |
| ---------- | ---- | ------- | ------- | ---- | ------------ | -------- |
| 文档类型及权限    | 连接数  | 文档所属用户  | 文档所属组   | 文档大小 | 文档最后被修改日期    | 文档名称     |

| -    | rw-           | r--              | r--           |
| ---- | ------------- | ---------------- | ------------- |
| 文档类型 | 文档所有者权限（user） | 文档所属用户组权限（group） | 其他用户权限（other） |

#### 文档类型

- `d` 表示目录
- `l` 表示软连接
- `–` 表示文件
- `c` 表示串行端口字符设备文件
- `b` 表示可供存储的块设备文件
- 余下的字符 3 个字符为一组。`r` 只读，`w` 可写，`x` 可执行，`-` 表示无此权限

#### 连接数

指有多少个文件指向同一个索引节点。

#### 文档所属用户和所属组

就是文档属于哪个用户和用户组。文件所属用户和组是可以更改的

#### 文档大小

默认是 bytes

### 更改操作权限

#### chown

是 change owner 的意思，主要作用就是改变文件或者目录所有者，所有者包含用户和用户组

`chown [-R] 用户名称 文件或者目录`

`chown [-R] 用户名称 用户组名称 文件或目录`

-R：进行递归式的权限更改，将目录下的所有文件、子目录更新为指定用户组权限

#### chmod

改变访问权限

`chmod [who] [+ | - | =] [mode] 文件名`

##### who

表示操作对象可以是以下字母的一个或者组合

- u：用户 user
- g：用户组 group
- o：表示其他用户
- a：表示所有用户是系统默认的

##### 操作符号

- +：表示添加某个权限
- -：表示取消某个权限
- =：赋予给定的权限，取消文档以前的所有权限

##### mode

表示可执行的权限，可以是 r、w、x

##### 文件名

文件名可以使空格分开的文件列表

##### 示例

```
lusifer@UbuntuBase:~$ ls -al test.txt 
-rw-rw-r-- 1 lusifer lusifer 6 Nov  2 21:47 test.txt
lusifer@UbuntuBase:~$ chmod u=rwx,g+r,o+r test.txt 
lusifer@UbuntuBase:~$ ls -al test.txt 
-rwxrw-r-- 1 lusifer lusifer 6 Nov  2 21:47 test.txt
lusifer@UbuntuBase:~$
```

### 数字设定法

数字设定法中数字表示的含义

- 0 表示没有任何权限
- 1 表示有可执行权限 = `x`
- 2 表示有可写权限 = `w`
- 4 表示有可读权限 = `r`

也可以用数字来表示权限如 chmod 755 file_name

| r w x | r – x | r - x  |
| ----- | ----- | ------ |
| 4 2 1 | 4 - 1 | 4 - 1  |
| user  | group | others |

若要 rwx 属性则 4+2+1=7

若要 rw- 属性则 4+2=6

若要 r-x 属性则 4+1=5

```
lusifer@UbuntuBase:~$ chmod 777 test.txt 
lusifer@UbuntuBase:~$ ls -al test.txt 
-rwxrwxrwx 1 lusifer lusifer 6 Nov  2 21:47 test.txt

lusifer@UbuntuBase:~$ chmod 770 test.txt 
lusifer@UbuntuBase:~$ ls -al test.txt 
-rwxrwx--- 1 lusifer lusifer 6 Nov  2 21:47 test.txt
```

## Linux 安装Java

此处以 JDK 1.8.0_152 为例

### 下载地址

http://www.oracle.com/technetwork/java/javase/downloads/index.html

### 解压缩并移动到指定目录

### 解压缩

```
tar -zxvf jdk-8u152-linux-x64.tar.gz
```

### 创建目录

```
mkdir -p /usr/local/java
```

### 移动安装包

```
mv jdk1.8.0_152/ /usr/local/java/
```

### 设置所有者

```
chown -R root:root /usr/local/java/
```

### 配置环境变量

### 配置系统环境变量

```
nano /etc/environment
```

### 添加如下语句

```
PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games"
export JAVA_HOME=/usr/local/java/jdk1.8.0_152
export JRE_HOME=/usr/local/java/jdk1.8.0_152/jre
export CLASSPATH=$CLASSPATH:$JAVA_HOME/lib:$JAVA_HOME/jre/lib
```

### 配置用户环境变量

```
nano /etc/profile
```

### 添加如下语句

```
if [ "$PS1" ]; then
  if [ "$BASH" ] && [ "$BASH" != "/bin/sh" ]; then
    # The file bash.bashrc already sets the default PS1.
    # PS1='\h:\w\$ '
    if [ -f /etc/bash.bashrc ]; then
      . /etc/bash.bashrc
    fi
  else
    if [ "`id -u`" -eq 0 ]; then
      PS1='# '
    else
      PS1='$ '
    fi
  fi
fi

export JAVA_HOME=/usr/local/java/jdk1.8.0_152
export JRE_HOME=/usr/local/java/jdk1.8.0_152/jre
export CLASSPATH=$CLASSPATH:$JAVA_HOME/lib:$JAVA_HOME/jre/lib
export PATH=$JAVA_HOME/bin:$JAVA_HOME/jre/bin:$PATH:$HOME/bin

if [ -d /etc/profile.d ]; then
  for i in /etc/profile.d/*.sh; do
    if [ -r $i ]; then
      . $i
    fi
  done
  unset i
fi
```

### 使用户环境变量生效

```
source /etc/profile
```

测试是否安装成功

```
root@UbuntuBase:/usr/local/java# java -version
java version "1.8.0_152"
Java(TM) SE Runtime Environment (build 1.8.0_152-b16)
Java HotSpot(TM) 64-Bit Server VM (build 25.152-b16, mixed mode)
```

### 为其他用户更新用户环境变量

```
su lusifer
source /etc/profile
```

## Linux 安装Tomcat

此处以 Tomcat 8.5.23 为例

### 下载地址

https://tomcat.apache.org/

### 解压缩并移动到指定目录

#### 解压缩

```
tar -zxvf apache-tomcat-8.5.23.tar.gz
```

#### 变更目录名

```
mv apache-tomcat-8.5.23 tomcat
```

#### 移动目录

```
mv tomcat/ /usr/local/
```

### 常用命令

#### 启动

```
/usr/local/tomcat/bin/startup.sh
```

#### 停止

```
/usr/local/tomcat/bin/shutdown.sh
```

### 目录内执行脚本

```
./startup.sh
```

## Linux 安装 MySql

### 安装

#### 更新数据源

```
apt-get update
```

#### 安装 MySQL

```
apt-get install mysql-server
```

系统将提示您在安装过程中创建 root 密码。选择一个安全的密码，并确保你记住它，因为你以后需要它。接下来，我们将完成 MySQL 的配置。

### 配置

因为是全新安装，您需要运行附带的安全脚本。这会更改一些不太安全的默认选项，例如远程 root 登录和示例用户。在旧版本的 MySQL 上，您需要手动初始化数据目录，但 Mysql 5.7 已经自动完成了。

运行安全脚本：

```
mysql_secure_installation
```

这将提示您输入您在之前步骤中创建的 root 密码。您可以按 Y，然后 ENTER 接受所有后续问题的默认值，但是要询问您是否要更改 root 密码。您只需在之前步骤中进行设置即可，因此无需现在更改。

### 测试

按上边方式安装完成后，MySQL 应该已经开始自动运行了。要测试它，请检查其状态。

```
lusifer@ubuntu:~$ systemctl status mysql.service
● mysql.service - MySQL Community Server
   Loaded: loaded (/lib/systemd/system/mysql.service; enabled; vendor preset: enabled)
   Active: active (running) since Tue 2017-11-21 13:04:34 CST; 3min 24s ago
 Main PID: 2169 (mysqld)
   CGroup: /system.slice/mysql.service
           └─2169 /usr/sbin/mysqld

Nov 21 13:04:33 ubuntu systemd[1]: Starting MySQL Community Server...
Nov 21 13:04:34 ubuntu systemd[1]: Started MySQL Community Server.
```

查看 MySQL 版本：

```
mysqladmin -p -u root version
```

### 配置远程访问

- 修改配置文件

```
nano /etc/mysql/mysql.conf.d/mysqld.cnf
```

- 注释掉(语句前面加上 # 即可)：

```
bind-address = 127.0.0.1
```

- 重启 MySQL

```
service mysql restart
```

- 登录 MySQL

```
mysql -u root -p
```

- 授权 root 用户允许所有人连接

```
grant all privileges on *.* to 'root'@'%' identified by '你的 mysql root 账户密码';
```

#### 因弱口令无法成功授权解决步骤

- 查看和设置密码安全级别

```
select @@validate_password_policy;
```

```
set global validate_password_policy=0;
```

- 查看和设置密码长度限制

```
select @@validate_password_length;
```

```
set global validate_password_length=1;
```

### 常用命令

#### 启动

```
service mysql start
```

#### 停止

```
service mysql stop
```

#### 重启

```
service mysql restart
```

### 其它配置

修改配置 `mysqld.cnf` 配置文件

```
vi /etc/mysql/mysql.conf.d/mysqld.cnf
```

#### 配置默认字符集

在 `[mysqld]` 节点上增加如下配置

```
[client]
default-character-set=utf8
```

在 `[mysqld]` 节点底部增加如下配置

```
default-storage-engine=INNODB
character-set-server=utf8
collation-server=utf8_general_ci
```

#### 配置忽略数据库大小写敏感

在 `[mysqld]` 节点底部增加如下配置

```
lower-case-table-names = 1
```

## 部署应用到生产环境

参考:https://www.bilibili.com/video/av27165701

## 附：Linux LVM 磁盘扩容

## LVM 的基本概念

### 物理卷 Physical volume (PV)

可以在上面建立卷组的媒介，可以是硬盘分区，也可以是硬盘本身或者回环文件（loopback file）。物理卷包括一个特殊的 header，其余部分被切割为一块块物理区域（physical extents）。

### 卷组 Volume group (VG)

将一组物理卷收集为一个管理单元。

### 逻辑卷 Logical volume (LV)

虚拟分区，由物理区域（physical extents）组成。

### 物理区域 Physical extent (PE)

硬盘可供指派给逻辑卷的最小单位（通常为 4MB）。

## 磁盘操作相关命令

### `df -h`（查看挂载点）

![](/Linux-img/003.png)

### `lvdisplay`（显示当前的 logical volume）

![](/Linux-img/004.png)

**备注：** 注意这里目前有两个，一个是文件系统所在的 `volume`，另一个是 `swap` 分区使用的 `volume`，当然，我们需要扩容的是第一个

### `vgdisplay`（显示当前的 volume group）

![](/Linux-img/005.png)

​	**备注：** 注意 `VG SIZE`，这里应该是你当前的可用空间大小，待扩容完毕，这里显示的应该是最终的大小

### `pvdisplay`（显示当前的 physical volume）

![](/Linux-img/006.png)

## 开始 LVM 扩容

### 查看 fdisk

```
fdisk -l
```

![](/Linux-img/007.png)

因为这台机器默认开启了 LVM，所以目前有一个 `extended` 分区和一个 `LVM` 分区，并且他们是完全重叠的。这是因为，LVM 分区作为一个虚拟的分区，完全占用了这个 extended 分区，原理图见下：

![](/Linux-img/008.png)

因此，现在需要做的就是将 extended partition (`sda2`) 扩展到最大，然后创建一个新的 LVM logical partition (`sda6`)，用它来填满 sda2

### 查看所有连接到电脑上的储存设备

```
fdisk -l |grep '/dev'
```

#### 1 块磁盘效果图

![](/Linux-img/009.png)

#### 2 块磁盘效果图（新增磁盘，尚未挂载）

![](/Linux-img/010.png)

### 创建 `sdb` 分区

```
fdisk /dev/sdb
n	# 新建分区
l	# 选择逻辑分区，如果没有，则首先创建扩展分区（p），然后再添加逻辑分区（硬盘：最多四个分区 P-P-P-P 或 P-P-P-E）
```

![](/Linux-img/011.png)

```
回车
回车
回车
w	# 写入磁盘分区
```

### 格式化磁盘

![](/Linux-img/012.png)

```
mkfs -t ext4 /dev/sdb1
```

![](/Linux-img/013.png)

### 创建 PV

```
pvcreate /dev/sdb1
```

### 查看卷组

```
pvscan
```

![](/Linux-img/014.png)

### 扩容 VG

```
vgdisplay
```

![](/Linux-img/015.png)

```
vgextend ubuntu-vg /dev/sdb1
```

### 扩容 LV

![](/Linux-img/016.png)

![](/Linux-img/017.png)

```
lvextend -L +30G /dev/ubuntu-vg/root
```

### 刷新分区

```
resize2fs /dev/ubuntu-vg/root
```

### 删除 unknown device

```
pvscan
vgreduce --removemissing ubuntu-vg
```

**注意：不要卸载扩容的磁盘，可能出现丢失数据或是系统无法启动**