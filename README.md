# Linux_note

## 目录

1_拷贝文件到本地，拷贝本地文件到远程服务器

拷贝远程服务器的文件到本地：
```
scp -P [端口号] [用户名]@[IP地址]:[服务器上的文件地址] [本地文件夹地址]
```

拷贝本地文件到远程服务器：
```
scp -P [端口号] [本地文件地址] [用户名]@[IP地址]:[服务器上的文件夹地址]
```

2_运行.sh文件
```
./[.sh文件]
```

3_crontab定时任务

4_centos7 更新Firefox版本
```
https://blog.csdn.net/swazer_z/article/details/64442471
```

5_查看进程
```
ps -ef
```

```
ps -ef | grep python
```
grep 是搜索

6_终止进程
```
kill -9 [PID]
```
-9 表示强迫进程立即停止

7_批量终止进程
```
pgrep firefox | xargs kill -s 9
```
关闭所有firefox的进程

8_压缩/解压缩
```
https://www.cnblogs.com/wangluochong/p/7194037.html
```

9_配置环境变量
```
cd ~
ll -a 
vi .bash_profile
source .bash_profile  # 重启.bash_profile使修改生效


GECKODRIVER_HOME=/home/···/software/geckodriver
export PATH=$PATH:$GECKODRIVER_HOME
```

10_磁盘格式化与挂载
```
磁盘使用情况
df -h

查看磁盘
fdisk -l

磁盘格式化
mkfs.ext4 /dev/sdl

挂载
mount /dev/sdl /home/user1/temp_test

取消挂载
umount /dev/sdl
```

11_查看CPU和内存使用情况
```
top  ps  pmap  free
```

```
Linux查看CPU和内存使用情况
https://www.cnblogs.com/mengchunchen/p/9669704.html

linux下查看CPU、内存、磁盘信息
https://www.cnblogs.com/xubiao/p/6497533.html
```

12_后台运行python脚本
```
https://www.cnblogs.com/master-pokemon/p/5790783.html
```
