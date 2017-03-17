LANMPS 一键安装包,php绿色环境套件包
=====================================
Linux+Nginx+Mysql+PHP+Elasticsearch ( phpmyadmin+opencache+xdebug )环境套件包,绿色PHP套件，一键自动安装

系统需求
-------------------------------------

* 系统：Linux下CentOS,RedHat,Ubuntu
* 内存：大于等于512M内存 
* 安装时需要联网

LANMPS 一键安装包V3.2.2 ：Linux+Nginx+Mysql+PHP+Elasticsearch ( phpmyadmin+opencache+xdebug )套件包,绿色PHP套件，一键自动安装。
> 
> 已在 CentOS7.x，Ubuntu17.x 中安装成功！
> 
> Apache 在下个版本中会实现


# 安装工具

SSH Secure Shell Client [下载 右击新窗口打开](http://soft.hao123.com/soft/appid/46598.html)

Xshell+Xftp (Windows 下推荐)

或者使用其他工具

使用`SSH Secure Shell Client`登陆服务器
# Lanmps 下载

安装包大小：340MB（包含相关环境所需文件）

### 方法二：
百度网盘下载(速度快)：[http://pan.baidu.com/s/1bnjIYKJ](http://pan.baidu.com/s/1bnjIYKJ)

然后上传文件到服务器上

# 安装
请以  `root`  用户执行命令

请以  `root`  用户执行命令

请以  `root`  用户执行命令

`重要的事情说3遍`
## 1.screen 安装启动
>screen 介绍
>screen 为了防止SSH登陆超时或掉线，中断安装（lanmps 为自定义名称）。
>如果掉线了，执行 
`screen -r lanmps`,即可恢复 掉线前的执行界面，如果忘记名字了，执行 `screen -ls` 会列出所有会话列表，其中`数字.lanmps`即为刚才的会话
>
>如果提示screen: command not found 命令不存在。
>
>CentOS 可以执行：`yum install -y screen`
>
>Ubuntu可以执行：`apt-get install -y screen`

>查看是什么系统的命令：`cat /etc/issue`

### CentOS 系统
```SHELL
yum install -y screen && screen -S lanmps
```
### Ubuntu 系统
```SHELL
apt-get install -y screen && screen -S lanmps
```
## 2.执行安装命令
>3.2.2 为版本号
>
>根据最新版本的版本号，更改下面相应的代码版本号
>
>`此版本改动较大`，有时php-fpm没有启动，请手动启动  /www/lanmps/php-fpm(`版本`) `start`
>
>如果你需要的套件是最新版本请修改相应的配置，并把相应的文件下载至down目录即可
>
>`mysql5.7版本 数据库默认密码为空`

在安装包的当前目录下执行：

`tar -zxvf lanmps-3.2.2.tar.gz && cd lanmps-3.2.2 && ./lanmps.sh`

## 2.2 执行上述命令后，会出现以下提示：选择安装套件类别（默认选1）

![](/doc/images/lanmps-01.png)

## 2.3 选择php版本（默认选则4）

![](/doc/images/lanmps-02.png)

## 2.4 选择Mysql版本（默认选则3）

![](/doc/images/lanmps-03.png)

## 2.5 提示”Press any key to start…”，按任意键开始安装

![](/doc/images/lanmps-04.png)

## 2.6 程序安装
到了这里，
LANMPS脚本就会自动编译安装Nginx、MySQL、PHP、phpMyAdmin、Opencache、Memcache、Xdebug,Elasticsearch,Redis 等软件。

其中Xdebug默认关闭，如需使用在php.ini开启。

安装时间可能会几十分钟到几个小时不等，主要是机器的配置网速等原因会造成影响。

## 2.7 安装完成
出现以下界面，则说明安装成功！

![](/doc/images/lanmps-05.png)

# LANMPS 状态管理命令
[LANMPS 状态管理命令](/lanmps-status.html)
# LANMPS 目录说明
[LANMPS 目录说明](/lanmps-file-list.html)
# 关于 LANMPS 
[关于 LANMPS ](/lanmps-about.html)
### 更新日志
* 2017年03月07日 LANMPS V3.2.2 发布

 * 升级PHP7.1.x
 * 升级MYSQL5.7.x
 * 升级REDIS
 * 升级NGINX1.11.x
 * BUG修复
 
* 2016年12月15日 LANMPS V3.2.0 发布

 * 升级PHP7.1
 * 升级MYSQL5.7
 * 升级REDIS
 * 升级NGINX1.11
 * BUG修复
 
* 2016年7月11日 LANMPS V3.1.0 发布

 * 升级PHP7
 * 升级MYSQL5.7
 * 升级REDIS
 * 升级NGINX1.10
 * 搜索引擎更换为 Elasticsearch
 * BUG修复
 
* 2015年7月16日 LANMPS V2.2.3 发布

 * php 版本更新
 * BUG修复

* 2015年1月31日 LANMPS V2.0.3 发布

 * 修复 apaache 加载 php BUG
 * BUG修复

* 2015年1月12日 LANMPS V2.0.1 发布

 * php 版本更新
 * MariaDB 数据库更新
 * nginx 版本更新
 * 可以更改任意安装目录
 * 支持 apache,可选apache安装
 * apache 支持按年月日分割日志
 * BUG修复
 * 优化部分参数

* 2014年12月22日 LANMPS V1.0.3 发布

 * php 版本更新
 * MariaDB 版本更新
 * nginx 版本更新
 * BUG修复
 
* 2014年11月1日 LANMPS V1.0.0 发布

 * php 版本更新
 * 增加MariaDB 数据库
 * nginx 版本更新
 * 增加sphinx搜索
 * 可以更改任意安装目录
 * 支持nginx日志自动分割(需设置linux定时任务)

* 2014年5月15日 LANMPS V0.2 发布

 * php 版本更新
 * 增加MariaDB 数据库
 * nginx 版本更新

* 2013年11月10日 LANMPS V0.1 发布

 * Nginx+Mysql+PHP+Opencache+Phpmyadmin+Xdebug 基础实现安装
 * Xdebug 默认关闭，如需开启，在php.ini中开启
 * Mysql 版本为 5.6.14，默认不能选择版本，以后版本中会实现
 * PHP 可以选择版本
 * Nginx为最新版1.5.6
 * 支持Linux 中的  Ubuntu 和 CentOS 系统

* 2013-09-09 LANMPS  项目开始