# Linux_note

## 拷贝文件到本地，拷贝本地文件到远程服务器
```
拷贝远程服务器的文件到本地：scp -r -P  端口号   用户名@IP地址:/usr/local/tomcat_airc/webapps/        /tmp/kyj/
拷贝本地文件到远程服务器：scp -r    /tmp/kyj/sys.war         用户名@IP地址:/usr/local/tomcat_airc/webapps/
```
