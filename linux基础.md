# linux认识  
## 简单介绍linux
Linux是一套免费使用和自由传播的类Unix操作系统，是一个基于POSIX和UNIX的多用户、多任务、支持多线程和多CPU的操作系统。它能运行主要的UNIX工具软件、应用程序和网络协议。支持32位和64位硬件。Linux继承了Unix以网络为核心的设计思想，是一个性能稳定的多用户网络操作系统。  
linux 正式版诞生于1991年10月5号，Linux可运行在 安卓系统的手机电脑、路由器、视频游戏控制台、台式计算机、大型机和超级计算机都是用的linux内核。  
主要特性编辑

#### 更多的介绍点击 [linux百度百科]（https://baike.baidu.com/item/linux/27050?fr=aladdin）
##  linux的安装
#### 安装centos7.5
在阿里镜像站或者其他一些知名机构的镜像站下载镜像包  ![阿里镜像站
]（https://mirrors.aliyun.com/centos/）点击7/--点击isos/--x86-64--CentOS-7-x86_64-Everything-1804.iso 点此即可下载。   
![下好后启动安装界面](https://img-blog.csdn.net/20170710163641800?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzMyMzM3Njg=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)  
![进入安装界面，选择系统语言，点击右下角的继续按钮]（https://img-blog.csdn.net/20170710163845028watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzMyMzM3Njg=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast）  
![选择日期时区]（https://img-blog.csdn.net/20170710164123504?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzMyMzM3Njg=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center）  
![软件项选着本地介质，软件选择 学习环境选桌面，工作环境选最小安装](https://img-blog.csdn.net/20170710164819490?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzMyMzM3Njg=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)  
## 分区：   

![可选自己分配](https://img-blog.csdn.net/20170710165527256?watermark/2/text/aHR0cDovL2Jsb2c) 
KDUMO这一项不去要启用，  
![最后以太网要开启  ](https://img-blog.csdn.net/20170710170004740?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzMyMzM3Njg=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)  
![然后开始安装即可](https://img-blog.csdn.net/20170710170117297?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzMyMzM3Njg=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)  
![接着就是安装过程喽,安装时可以创建root用户密码和创建用户名。。。](https://img-blog.csdn.net/20170710170254140?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcXFfMzMyMzM3Njg=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)  
# 安装完后就可以使用啦  
 用图形界节省生内存   
 ```bash
 [root@centos7 ~]#free -h
              total        used        free      shared  buff/cache   available
Mem:           1.9G        228M        1.1G        9.9M        580M        1.5G
Swap:          4.0G          0B        4.0G
    
    id -u  查看本账号的id  例如id -u不带用户名查看root id   
[root@bogon ~]# id -u
0
[root@bogon ~]# id -u caixiaoyang
1000
  
  bc计算器
cal 日历
cd切换工作目录；不带任何参数时即切换到家目录
     ～[#：～ cd   带波浪线表示切换到自己的家目录 ？
     ～]#：cd ～USERNAME 切换到指定用户的家目录 还不懂
     ～]#: cd -     在上一次所在的目录与当前目录之间来回切换 

cd .. 的用法  返回上一级的目录：
[root@bogon sysconfig]# cd ..
[root@bogon etc]# cd .. /var/log
[root@bogon /]# cd ../var/log
[root@bogon log]# 

cd相对路径的使用：
[root@bogon log]# cd /var/log/audit
[root@bogon audit]# cd ..
[root@bogon log]# cd audit/或者cd ./audit/也可
[root@bogon audit]# 
$PWD：当前工作目录
$OLDPWD:查看上一个工作目录  例如:
                                                      root@bogon audit]# echo $PWD
                                                      /var/log/audit
                                                      [root@bogon audit]# echo $OLDPWD
                                                      var/log
                                                      [root@bogon audit]# 
ls -a列出所有 含隐藏文件
   -A列出除.  .. 之外的所有文件；
   -l  列出除隐藏文件外的所有文件，目录详细信息 权限 所属主 所属主 日期
   -h  文件大小换算  非精确  ；
   -d  查看目录本身而非其内部的文件列表；
   -r   逆序显示。从z到a顺序排序
 
ls -l  /usr/bin/x*查看x开头的文件

ls -l -h /var/log 
 rw-r--r--. 1 root   root          8957       10月 14日 19：22 boot.log
-：文件类型，- ，d，c，l，  s，p
rw-r--r--
             rw-:文件属主的权限；
             r--文件属组的权限；
             r--：其他用户（非属主，属组）的权限；
1：数字表示文件被连接的次数；
root：文件的属主
root：文件的属组；
8957：数字表示文件的大小，单位是字节
 10月 14日 19：22 boot.log：最近一次修改的时间；

file:查看文件内容类型  
[root@bogon etc]#  file /etc/passwd
/etc/passwd: ASCII text

cat：文本文件查看工具，不能查看bin 二进制程序
-n：显示文本行序列号
-E：行尾加上$符
cat -nE /etc/fatab
功能同上反过来显示文本信息：tac：文本文件查看工具，不能查看bin 二进制程序
-n：显示文本行序列号
-E：行尾加上$符
tac -nE /etc/fatab  

  alias 别名：
[root@centos6 ~]#cd /etc/sysconfig/network-scripts/  （输入的命令多）
[root@centos6 network-scripts]#alias cdnet="cd /etc/sysconfig/network-scripts/"（用别名定制）此时已经存到硬盘里  内存还没读取生效，
要执行：
[root@centos6 ~]#source .bashrc 
还可以执行： . . bashrc(第一个点相当source)
就可以及时生效。
source读臊斯  
source 后面跟修改过的路径就可以及时生效
这是root用户才生效 普通用户：  
 先进入 cd /home/caixiaoyang
nano .bashrc 更改
要想全部用户生效可以：
nano /etc/bashrc  改这个文件就可以全部生效 生效：. /etc/bashrc  
查看ram使用
[root@centos7 ~]# free -h
              total        used        free      shared  buff/cache   available
Mem:           1.9G（总共的）        211M（已使用的）        1.2G        9.9M        511M        1.5G
Swap:          4.0G          0B        4.0G  
查看当前提示符格式
[root@centos7 ~]# echo $PS1
[\u@\h \W]\$  
root@centos7 ~]#nano /etc/profile.d/env.sh进入命令提示符文件
进入后写入;
PS1="\[\[1;5;41;33m\][\u@\h \W]\\$\[\e[0m\]" 推出保存即可PS1="\[\e[1;33m\][\u@\h \W]\\$\[\e[0m\]"
ntpdate 172.16.0.0 同步这台主机的时间  lock-s 同步硬件的时间
-w同步系统的时间    
```

### 开机自动启动
```bash   
nano /etc/gdm/custom.conf
                 在【daemon】选项下写
                 AutomaticLoginEnable=true
                 AutomaticLogin=root or其他用户名  
                 ```
                 
反向单引号最聪明   可以全部计算单引号里的命令
```bash
ls -l `echo $SHELL`
ls -l     $（echo $SHELL）跟上面的一样效果
{}花括号 ：
[root@centos7 ~]#echo file{aa,bb,cc}
fileaa filebb filecc
[root@centos7 ~]#echo file{aa,bb,cc}.{txt,log}
fileaa.txt fileaa.log filebb.txt filebb.log filecc.txt filecc.log

[root@centos7 ~]#echo {1..9}
1 2 3 4 5 6 7 8 9
[root@centos7 ~]#echo {1..100..2}
1 3 5 7 9 11 13 15 17 19 21 23 25 27 29 31 33 35 37 39 41 43 45 47 49 51 53 55 57 59 61 63 65 67 69 71 73 75 77 79 81 83 85 87 89 91 93 95 97 99  （每次加2）
[root@centos7 ~]#echo {a..z}
a b c d e f g h i j k l m n o p q r s t u v w x y z  
```
帮助
whatis ls  查看ls这个命令是干嘛的、=man -f ls相同的

makewhatis 创建whatis（centos6专用）
mandb创建whatis centos7专用
ll为ls-l 
```bash 
[root@centos7 ~]#ll /etc/fstab  /etc/motd 
-rw-r--r--. 1 root root 595 Sep 20 09:38 /etc/fstab
-rw-r--r--. 1 root root  21 Sep 20 17:03 /etc/motd
[root@centos7 ~]#!*:p 显示上个命令参数
/etc/fstab /etc/motd
[root@centos7 ~]#ll !*打印最后一个参数
ll /etc/motd
-rw-r--r--. 1 root root 21 Sep 20 17:03 /etc/motd  
history 历史命令记录[root@centos7 ~]#ls -a
.                .bash_history  .bashrc  .cshrc   Documents  FLAMING_MOUNTAIN.JPG  .local    Public     Videos
..               .bash_logout   .cache   .dbus    Downloads  .ICEauthority         Music     .tcshrc    .Xauthority
anaconda-ks.cfg  .bash_profile  .config  Desktop  .esd_auth  initial-setup-ks.cfg  Pictures  Templates
[root@centos7 ~]#nano .bash_history 
 清楚历史命令痕迹：
[root@centos7 ~]#rm -f .bash_history 先删除历史文件
[root@centos7 ~]#history -c再清除历史
[root@centos7 ~]#history -d 3 删除第三条内存ram历史记录
history -a 附加历史命令
history -w 把现在的历史写入文件中
[root@centos7 ~]#history -s 'rm -rf /'伪造历史

[root@centos7 ~]#HISTTIMEFORMAT="%F %T"历史命令加入时间
touch建 -a  加上两个杠
 [root@centos7 ~]#touch  -- -a
删除-a文件 ：[root@centos7 ~]#rm -- -a
rm：是否删除普通空文件 "-a"？y
[root@centos7 ~]#cd /data/
[root@centos7 data]#ls
[root@centos7 data]#touch  ./-a
[root@centos7 data]#ls
-a（用相对路径也能创建文件  用./表示当前路径下 创建-a文件）
```