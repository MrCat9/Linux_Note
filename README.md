# Linux_note

## 目录

#### 1_拷贝文件到本地，拷贝本地文件到远程服务器

拷贝远程服务器的文件到本地：
```
scp -P [端口号] [用户名]@[IP地址]:[服务器上的文件地址] [本地文件夹地址]
```

拷贝本地文件到远程服务器：
```
scp -P [端口号] [本地文件地址] [用户名]@[IP地址]:[服务器上的文件夹地址]
```

#### 2_运行.sh文件
```
./[.sh文件]
```

#### [3_crontab定时任务](https://github.com/MrCat9/Linux_Note/blob/master/crontab_task.md)

#### 4_centos7 更新Firefox版本
```
https://blog.csdn.net/swazer_z/article/details/64442471
```

#### 5_查看进程
```
ps -ef
```

```
可以用 grep 搜索
ps -ef | grep python
```

```
在Linux中查看所有正在运行的进程
https://www.cnblogs.com/zwgblog/p/5971455.html
```

#### 6_终止进程
```
kill -9 [PID]
```
-9 表示强迫进程立即停止

#### 7_批量终止进程
```
pgrep firefox | xargs kill -s 9
```
关闭所有firefox的进程
```
Linux下强制杀死进程的方法
https://www.cnblogs.com/liaojie970/p/7131043.html
```

#### 8_压缩/解压缩
```
https://www.cnblogs.com/wangluochong/p/7194037.html
```

#### 9_配置环境变量
```
cd ~
ll -a 
vi .bash_profile
source .bash_profile  # 重启.bash_profile使修改生效


GECKODRIVER_HOME=/home/···/software/geckodriver
export PATH=$PATH:$GECKODRIVER_HOME
```

#### 10_[磁盘格式化与挂载](https://www.cnblogs.com/cc66/p/9414718.html)
```
磁盘使用情况
df -h

查看磁盘
fdisk -l

查看系统检测的磁盘
lsblk

磁盘格式化
mkfs.ext4 /dev/sdl

挂载
mount /dev/sdl /home/user1/temp_test

取消挂载
umount /dev/sdl

查看占用磁盘的进程
fuser -m -v /dev/sdl

取消挂载 umount 时出现的 “Device is busy”
https://blog.csdn.net/a1232345/article/details/46710989/
```

#### 11_查看CPU和内存使用情况
```
top  ps  pmap  free
```

```
Linux查看CPU和内存使用情况
https://www.cnblogs.com/mengchunchen/p/9669704.html

linux下查看CPU、内存、磁盘信息
https://www.cnblogs.com/xubiao/p/6497533.html
```

#### 12_后台运行python脚本
```
python /···/my_python.py > my_python.log &
```
```
linux 下后台运行python脚本
https://www.cnblogs.com/master-pokemon/p/5790783.html
```

#### 13_文件权限
```
Linux命令:修改文件权限命令chmod、chgrp、chown详解
https://www.cnblogs.com/Berryxiong/p/6193866.html
```

#### 14_ln
```
ln -s /usr/local/python3/bin/python3 /usr/bin/python3

Linux软链接的创建，删除，修改
https://blog.csdn.net/weixin_40744265/article/details/87916847

ln命令创建和删除软、硬链接
https://www.cnblogs.com/klb561/p/9240758.html

在文件之间建立链接（硬链接和软链接）详解版
http://c.biancheng.net/view/740.html
```

#### 15_孤儿进程与僵尸进程
```
https://www.cnblogs.com/Anker/p/3271773.html
```

#### 16_显示文件的最后几行
```
显示 filename 的最后10行
tail -n 10 filename
```

#### 17_shell脚本删除X天前的日志

https://blog.csdn.net/weixin_33691817/article/details/93494414

https://blog.csdn.net/lylload/article/details/79231655

```sh
#!/bin/bash
find /opt/soft/log/ -mtime +30 -name "*.log" -exec rm -rf {} \;
```

#### 18_查看文件指定行

```
分页
cat filename.txt | more

从第3000行开始，显示1000行，也就是3000~3999
cat filename.txt | tail -n +3000 | head -n 1000

只查看文件的第5行到第10行
sed -n '5,10p' filename.txt
```
查看某个文件指定行信息（前n行，后n行） https://blog.csdn.net/qq_21997625/article/details/89460657

#### [19_nginx负载均衡](https://github.com/MrCat9/Linux_Note/blob/master/nginx_load_balancing_test.conf)

https://www.jianshu.com/p/3c4caf00a73d

https://www.cnblogs.com/HeiDi-BoKe/p/11417155.html

#### 20_xshell无法连接远程服务器

```
有的能连上有的连不上。可能是因为IP进了黑名单。

查看黑名单列表
cat /etc/hosts.deny

从黑名单中删除该IP
sudo vim /etc/hosts.deny
```

#### 21_查看公网/外网IP

```
curl httpbin.org/get
curl icanhazip.comcurl icanhazip.com
```

#### 22_使用`tinyproxy`搭建代理服务器

linux下搭建HTTP代理服务器 https://blog.csdn.net/zzggb/article/details/105201608

#### 23_虚拟机下的虚拟机

```
无法在虚拟机上再创建虚拟机。
在Windows虚拟机上可以安装virtual box，但无法创建Ubuntu虚拟机。

无法在Windows虚拟机上安装docker。
docker基于Linux运行，Windows上的docker需要跑在Linux虚拟机上。
```

#### 24_网络故障排查

网络故障排查 https://blog.csdn.net/weixin_39755824/article/details/109828882

#### 25_[bashrc与profile的区别](https://www.cnblogs.com/yuanqiangfei/p/10232148.html)