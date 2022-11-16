# 有外网动态IP无80端口自建多个网站梳理

## 1、安装

brew install mysql

## 2、配置原理

### 2.1 mac nginx默认是8080端口，不用修改，路由器上转发一个可用端口（例如580）到Mac服务器的8080端口。
### 2.2 将域名bj.beyondthe.top动态解析（DDNS）到路由器外网IP，换别的动态域名（如路由器自带）的时候，把bj.beyondthe.top CNAME解析到路由器自带域名。
### 2.3 创建子网站的beyondthe.top二级域名，如example.beyondthe.top，CNAME解析到bj.beyondthe.top
### 2.4 在Mac服务器创建网站目录/Volumes/RAID1/www/example.org
### 2.4 在Mac服务器创建子网站nginx配置文件/usr/local/etc/nginx/servers/example.org.conf的配置文件，通过nginx -s reload命令更新配置文件，

## 3、测试

互联网测试地址 http://example.beyondthe.top:580
局域网测试地址 http://example.beyondthe.top:8080
没有解析域名或者解析还没生效可以通过编辑host测试网站。
sudo vim /etc/hosts

## 4、上线

将网站真实域名(例如example.org)隐性转发/使用带掩码转发到 http://example.beyondthe.top:580
