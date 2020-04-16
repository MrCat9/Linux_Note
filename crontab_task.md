cmd下

# 查看crontab列表
crontab -l

# 编辑crontab列表
crontab -e

# 查看crontab运行日志
sudo cat /var/log/cron




# 要设置一个定时python程序的话（3步）：
1. 写一个shell脚本
```
vi run_spider_sh.sh
```
内容：
```
#!/bin/sh
cd /home/···/spider    -->cd到python程序所在的文件夹
/usr/local/bin/python3 test_spider.py    -->运行python程序
echo "yes" >> /home/···/test.txt    -->将 yes 写到test.txt里
```
注意：
```
摘自： https://www.jb51.net/article/65147.htm
报错： ^M: 坏的解释器: 没有那个文件或目录
原因： 这个问题大多数是因为sh脚本文件在windows下编辑过。
    windows下，每一行的结尾是\n\r，而在linux下文件的结尾是\n，
    那么在windows下编辑过的文件在linux下打开看的时候每一行的结尾就会多出来一个字符\r,
    用cat -A urfile时你可以看到这个\r字符被显示为^M，这时候只需要删除这个字符就可以了。
    可以使用命令sed -i 's/\r$//' urfile 。
```


2. 给sh赋予运行权限
chmod +x /home/···/run_spider_sh.sh


3. 设置定时运行sh
crontab -e

30 22 * * * /home/···/run_spider_sh.sh  -->每天22:30运行run_spider_sh.sh    -->分钟 小时 天 月 星期 要执行的命令

# 报错："/var/spool/cron/tmp.XXXXFSq8E3: 权限不够"

https://blog.csdn.net/weixin_43822878/article/details/104053015



