---
author: stannis
date: 2012-3-10 11:50+08:00
layout: post
title: XP上安装APACHE2.2.15和PHP5.2.14(win7 32位同样适用)
slug: 
categories:
- 网站架设
tags:
- Apache
---
### 1：下载并安装APAPCHE2.2.15 ###
下载地址：
[http://archive.apache.org/dist/httpd/binaries/win32/httpd-2.2.15-win32-x86-no_ssl.msi](http://archive.apache.org/dist/httpd/binaries/win32/httpd-2.2.15-win32-x86-no_ssl.msi)

把路径改为C:\APACHE，其它按默认选项安装。

![](http://ww4.sinaimg.cn/mw600/40a4b918jw1dquk386xtbj.jpg)

<!--more-->
安装完毕后，apache会自动启动，右下角状态栏会有一个绿色的apache服务器运行图标，如下图所示：

![](http://ww2.sinaimg.cn/mw600/40a4b918jw1dquk332lw2j.jpg)

打开浏览器，地址栏里输入：127.0.0.1，如果出现“It works.”，那么apache就已经安装成功了

![](http://ww2.sinaimg.cn/mw600/40a4b918jw1dquk3wz83mj.jpg)

### 2：下载并配置PHP5.2.14VC6，TS版 ###
下载地址：[http://windows.php.net/downloads/releases/php-5.2.14-Win32-VC6-x86.zip](http://windows.php.net/downloads/releases/php-5.2.14-Win32-VC6-x86.zip)

在C盘根目录新建文件夹PHP，把下载的文件解压到PHP文件夹。
将PHP文件夹（C:\PHP）下的 php.ini-dist 文件重命名为 php.ini，做如下修改：

- extension_dir的值更改为：

    extension_dir=”C:\PHP\ext”

- default_charset行首的分号去掉，并把值更改为

    default_charset = “utf-8″

- register_globals=Off 改为 

    register_globals=On

把下面几行代码句首的分号去掉

    extension=php_dba.dll
    extension=php_dbase.dll
    extension=php_gd2.dll
    extension=php_mbstring.dll
    extension=php_mcrypt.dll
    extension=php_mysql.dll
    
把修改好的 php.ini 文件复制到 C：\WINDOWS\ 目录。

把PHP目录下的 php5ts.dll libmcrypt.dll libmysql.dll三个文件复制到 C:\WINDOWS\system32 目录。

### 3：配置APACHE的httpd.conf文件添加对PHP的支持。 ###

用记事本打开C:\Apache\conf目录下的httpd.conf文件

把“DirectoryIndex index.html”修改为：“DirectoryIndex index.html index.php”（就是在原值后面加一个半角空格和index.php）

找出如下代码

    <Directory />
    Options FollowSymLinks
    AllowOverride None
    Order deny,allow
    deny from all
    </Directory>

将其修改为：

    <Directory />
    Options FollowSymLinks
    AllowOverride None
    Order deny,allow
    allow from all
    </Directory>

在文件最后加上如下两行代码

    LoadModule php5_module C:/PHP/php5apache2_2.dll
    AddType application/x-httpd-php .php
 
### 4：重启APACHE，测试配置是否成功 ###
把C:\Apache\htdocs下的index.html扩展名改为php,添加代码

{% highlight php %}
<?php
  phpinfo();
?>
{% endhighlight %}

保存index.php，在浏览器中打开127.0.0.1回车查看，出现下图即表示安装配置成功。

![](http://ww4.sinaimg.cn/mw600/40a4b918jw1dquk4wrapej.jpg)
