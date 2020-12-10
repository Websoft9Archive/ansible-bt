# 更多...

下面每一个方案，都经过实践证明行之有效，希望能够对你有帮助

## 域名绑定

绑定域名的前置条件是：已经完成域名解析（登录域名控制台，增加一个A记录指向服务器公网IP）  

完成域名解析后，从服务器安全和后续维护考量，需要完成**域名绑定**：

BT 域名绑定操作步骤：

![](http://libs.websoft9.com/Websoft9/DocsPicture/zh/btlinux/bt-linux-mdomain-websoft9.png)

一般来说新增网站首先就要填写域名。如果是修改网站，先删除就域名，然后再增加域名

## 挂载数据盘

宝塔镜像默认安装都在系统盘，如果您购买了额外的数据盘，如何挂载呢？

1. 将数据盘格式化
2. 面板设置-默认建站目录，将C:\wwwroot目录更改为数据盘对应的目录
![](http://libs.websoft9.com/Websoft9/DocsPicture/zh/btwin/btwin-wwwroot-websoft9.png)

注意：如果已有多个网站，建议先完成如下两个操作以不影响原网站：
1. 先将wwwroot的数据备份下来
2. 将原wwwroot中的文件拷贝到数据盘对应的目录
3. 通过网站管理修改网站路径

## 安装PHP扩展

打开宝塔面板->软件管理，找到PHP，点击设置，我们会看到“安装扩展项”

![](http://libs.websoft9.com/Websoft9/DocsPicture/zh/btwin/btwin-phpset-websoft9.png)

安装完成后，请点击“PHP服务”重启服务

## 设置HTTPS

宝塔中设置HTTPS两种方式，请根据您的实际情况进行选择：

* 注册宝塔官方账号，绑定后一键完成HTTPS部署
* 自行上传SSL证书，完成部署。（[官方帮助](https://www.bt.cn/bbs/thread-704-1-1.html)）

> 宝塔SSL申请的是免费版TrustAsia DV SSL CA - G5(1年）

## 找回BT面板密码

当忘记了宝塔Web端密码时，请远程桌面到Windows服务器，打开客户端->右上角菜单->修改密码 ，即可修改用户名和密码

![宝塔Windows 重置密码](http://libs.websoft9.com/Websoft9/DocsPicture/zh/btwin/bt-winresetpw-websoft9.png)

## 查看和管理日志文件

日志文件是诊断故障和问题的重要手段，宝塔使用中可能会用到与日志相关的操作包括：

####  宝塔面板操作日志

登录宝塔面板->安全，会看到面板操作日志，点击“清空”按钮会清空所有操作记录

![](http://libs.websoft9.com/Websoft9/DocsPicture/zh/btlinux/btlinux-panellogs-websoft9.png)

#### Web日志、网站日志

通过宝塔在线文件管理，进入：C:\BtSoft\WebSoft\apache\logs 目录，管理Web日志、网站日志

## 管理数据库

在宝塔面板中，尽量使用 phpMyAdmin 来管理数据库

1. 进入宝塔面板-数据库，找到root密码和phpMyAdmin链接
    ![](http://libs.websoft9.com/Websoft9/DocsPicture/zh/btlinux/bt-linux_phpmyadmin-websoft9.png)
2. 点击“root密码”，设置好您的默认密码
2. 点击phpMyAdmin，输入root和对应的密码，然后登录到系统中
    ![](http://libs.websoft9.com/Websoft9/DocsPicture/zh/mysql/phpmyadmin-logincn-websoft9.png)

> 阅读Websoft9提供的 [《MySQL教程》](https://support.websoft9.com/docs/mysql/zh/admin-phpmyadmin.html) ，掌握更多的MySQL实用技能：修改密码、导入/导出数据、创建用户、开启或关闭远程访问、日志配置等

## 重置（修改）MySQL密码

对于宝塔面板来说，重置密码与修改密码是同样的操作。

进入宝塔面板->数据库，点击“root密码”链接，修改后点击提交即可

![](http://libs.websoft9.com/Websoft9/DocsPicture/zh/btlinux/btlinux-mysqlpw-websoft9.png)