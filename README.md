# Linux_note

## 拷贝文件到本地，拷贝本地文件到远程服务器

拷贝远程服务器的文件到本地：
```
scp -P [端口号] [用户名]@[IP地址]:[服务器上的文件地址] [本地文件夹地址]
```

拷贝本地文件到远程服务器：
```
scp -P [端口号] [本地文件地址] [用户名]@[IP地址]:[服务器上的文件夹地址]
```

## 运行.sh文件
```
./[.sh文件]
```

## crontab定时任务

## centos7 更新Firefox版本
```
https://blog.csdn.net/swazer_z/article/details/64442471
```

## 查看进程
```
ps -ef
```

```
ps -ef | grep python
```
grep 是搜索

## 终止进程
```
kill -9 [PID]
```
-9 表示强迫进程立即停止

## 批量终止进程
```
pgrep firefox | xargs kill -s 9
```
关闭所有firefox的进程

## 压缩/解压缩
```
https://www.cnblogs.com/wangluochong/p/7194037.html
```
