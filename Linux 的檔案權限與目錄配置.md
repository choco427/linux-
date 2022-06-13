# Linux 的檔案權限與目錄配置
* owner		        所有者 
* group		        组成员 
* others		        其他成员
* /etc/passwd	        保存用户信息
* /etc/shadow	        保存用户密码
* /etc/group	        保存用户组
* ls -al		        列出所有的档案详细权限与属性 (包含隐藏文件)
* cp		        拷贝档案
* cd		        变更目录
* mkdir		        建立目录
* touch		        建立空档案
* su		        切换用户(switch user)
* rm		        删除目录或档楼(remove)
* cat                     读取档案内容
* uname                   打印系统信息
* lsb_release             显示LSB和特定版本的相关信息
* ls -al 后显示信息,如下：
* drwxrwxr-x	        档案类型权限
* 3 		        连结数
* luoliang 	        档案拥有者
* luoliang 	        档案所属群组
* 4096 		        档案大小(bytes)
* 12月 16 19:08 	        最后修改时间
* works		        档案名称

### 档案类型权限第一个字符代表档案类型：
* 当为[ d ]则是目彔
* 当为[ - ]则是档案
* 若是[ l ]则表示为连结档(link file)
* 若是[ b ]则表示为装置文件里面的可供储存的接口设备(可随机存取装置)
* 若是[ c ]则表示为装置文件里面的串行端口讴备

### 档案种类：
* 普通档案 regular file [ - ] 包括：纯文本文档、二进制文件、数据格式文件。
* 目录 directory [ d ]
* 连接档 link [ l ]
* 区块设备档 block [ b ]
* 字符设备文件 character [ c ]
* 资料接口文件 sockets [ s ]
* 数据输送文件 FIFO,pipe [ p ]


### 接下来的字符中，以三个为一组，且均为 [ rwx ] 的三个参数的组合。其中：
* [ r ]代表可读(read)
* [ w ]代表可写(write)
* [ x ]代表可执行(execute)


### Linux目录配置的依据-FHS
* /                     根目录
* /bin                  一般身份可执行文件
* /sbin                 系统管理员可用指令
* /dev                  系统装置档案
* /usr                  软件 Unix Software Resource
* /usr/X11R6            X Window System 重要数据
* /usr/bin              大部分用户指令
* /usr/include          程序语言的档头与包含档
* /usr/lib              应用软件函数库、目标档案等
* /usr/local            系统管理员自行安装的软件
* /usr/sbin             非系统正常运作所需要的系统指令
* /usr/share            共享文件
* /usr/share/man        联机帮助文件    
* /usr/share/doc        软件的文件说明
* /usr/share/zoneinfo   时区档案
* /usr/src              一般原始码
* /usr/src/linux        核心原始码
* /opt                  第三方软件
* /boot                 开机与核心档
* /home                 系统默认的用户家目录
* /root                 root用户的家目录
* /lib                  开机使用的函数库
* /media                可移除装置 如软盘光盘
* /mnt                  挂载装置
* /srv                  网络服务相关数据
* /tmp                  临时文件
* /etc                  配置文件
* /etc/init.d           所有服务的预设启动脚本
* /etc/xinetd.d         super daemon管理服务的配置文件
* /etc/X11              X Window 相关配置文件
* /var                  与系统运作过程相关
* /var/mail             邮箱
* /var/run              程序相关
* /var/lock             装置或档案锁
* /var/cache            应用程序缓存文件
* /var/lib              程序需要使用的数据文件
* /var/log              登录日志文件
* /var/run              程序启动后PID放置的目录
* /var/spool            队列数据
* /lost+found           文件系统发生错误时将一些遗失的片段放置到此目录
* /proc                 此目录放置的数据都保存在内存中，如系统核心、进程信息、网络状态等信息
* /sys                  记录核心相关信息，数据保存在内存中

### 不可与根目录分开的目录:
* /etc
* /bin
* /dev
* /lib
* /sbin
