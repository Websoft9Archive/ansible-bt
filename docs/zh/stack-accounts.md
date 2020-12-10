# 账号密码

使用BT，可能会用到的几组账号密码如下：

## BT

宝塔 Linux 和 Windows 版对应的账号密码以及登录方式不同：

### Linux 版 

* 管理员用户名：`administrator`  
* 管理员密码：`admin123`    
* 登录方式：*http://服务器公网IP:8888*

> 密码安全性提示：BT密码是为了帮助您简化安装和使用的，但默认密码并不安全，因此在完成镜像安装之后，立即通过管理地址修改默认密码。

### Windows 版
**宝塔6.9及以上版本**

与Linux版本统一登录方式

管理员用户名：`administrator`  
管理员密码：`admin123`    
登录方式：*http://服务器公网IP:8888*

**宝塔6.9以下版本**

* 登录方式：*http://服务器公网IP:888*  或 远程桌面到服务器访问BT客端户  
* 账号密码：需远程桌面到服务器通过BT客户端进行密码初始化  


## 操作系统

### Linux

* 主机地址：服务公网IP地址
* 连接方式：云控制台在线SSH 或 SFTP客户端工具 或 SSH客户端工具
* 管理员密码：创建服务器的时候自行设置，若不记得密码需要通过云控制台重置。
* 管理员账号：不同的云平台有一定的差异
   |  云平台   |  管理员账号   | 其他|
   | --- | --- | --- |
   |  Azure   |  创建服务器的时候自行设置   | [如何开启root账户？](https://support.websoft9.com/docs/azure/zh/server-login.html#示例2：启用系统root账号) |
   |  AWS Centos 系统   |  centos   | [如何开启root账户？](https://support.websoft9.com/docs/aws/zh/server-login.html#示例2：启用系统root账号) |
   |  AWS Ubuntu 系统  |  ubuntu   | [如何开启root账户？](https://support.websoft9.com/docs/aws/zh/server-login.html#示例2：启用系统root账号)  |
   |  阿里云，华为云，腾讯云   |  root   | |

### Windows

* 主机地址：服务公网IP地址
* 连接方式：云控制台在线管理 或 远程桌面工具
* 管理员密码：创建服务器的时候自行设置，若不记得密码需要通过云控制台重置。
* 管理员账号：不同的云平台有一定的差异
   |  云平台   |  管理员账号   |
   | --- | --- |
   |  Azure   |  创建服务器的时候自行设置   |
   |  AWS，阿里云，华为云，腾讯云   |  administrator   |
