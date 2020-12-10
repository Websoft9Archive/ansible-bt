# 初始化安装

在云服务器上部署 BT（Windows） 预装包之后，请参考下面的步骤快速入门。

* Windows平台宝塔6.9及以上版本已与Linux平台的访问方式统一： [Linux初始化安装](/zh/stack-installation.md#准备)
*下列内容是Windows平台宝塔6.9以下版本操作方式

## 准备

1. 在云控制台获取您的 **服务器公网IP地址** 
2. 在云控制台安全组中，检查 **Inbound（入）规则** 下的 **TCP:888** 端口是否开启
3. 若想用域名访问 BT，请先到 **域名控制台** 完成一个域名解析

### Web 后台初始化

此时，仍然不能使用 Web 版后台（[桌面端和Web端](/zh/win/stack-installation.md#桌面端和web端)），需要先远程连接到服务器，完成进行**初始化设置**后，方能访问 Web 端。

1. 远程桌面到服务器->打开Windows面板软件端，打开软件右上角的菜单，选择（初始化/修改密码）功能，输入您的账号和密码
   ![](http://libs.websoft9.com/Websoft9/DocsPicture/zh/btwin/btwin-inti-websoft9.png)
2. 本地电脑打开浏览器，访问：http://服务IP:888 ，使用上一步设置的密码登录进入Web后台
   ![](http://libs.websoft9.com/Websoft9/DocsPicture/zh/btwin/bt-winbackend-websoft9.png)
3. 如果有更新提示，请先点击“立即更新”后再使用宝塔


> 注意：宝塔的历史版本，是直接通过http://服务IP:888 设置后台密码的  

  ![](http://libs.websoft9.com/Websoft9/DocsPicture/zh/btwin/bt-winstart-websoft9.png)

## 网站环境安装

镜像中只安装了干净的面板工具。登录面板工具-->软件管理-->运行环境

![](http://libs.websoft9.com/Websoft9/DocsPicture/zh/btwin/bt-win-intallhj-websoft9.png)

参考上图，找到需要安装的软件，点击安装即可

## 常见问题

#### 浏览器无法访问 BT（白屏没有结果）？

您的服务器对应的安全组 888 端口没有开启（入规则），且没有远程桌面初始化宝塔之前，浏览器无法访问到服务器的任何内容

#### 能否将 PHP, Java 和 Node.js 安装到一起？

可以，但不建议。虽然宝塔的功能强大，能够安装的组件足够多，但是请把握一个原则，能不装的不要装，现在用不到的不要装

#### 需要运行PHP网站怎么安装环境？

分别安装Apache，MySQL，PHP，环境即搭建完成

#### 安装哪个PHP版本？

如果软件没有特殊要求，建议安装PHP7.0版本。另外，除非有多版本需求，请不要主动安装多个PHP版本

#### 哪些是必须安装的？

本质上没有必须安装的软件，请根据应用要求去安装所需的软件。一个重要原则“能不装的都不要装”

#### SQLServer怎么安装？

SQLServer需要远程桌面到服务器，通过服务器上的BT客户端进行安装

#### IIS与Apache，Nginx可以都安装吗？

宝塔中IIS与Apache或Nginx会冲突，请勿安装IIS

#### 宝塔可以使用IIS吗？

宝塔主要为PHP应用而生，如果使用IIS，宝塔面板存在的必要性不高。

## 桌面端和Web端

BT面板Windows版本有两个客户端可以访问BT，一个是服务器的桌面端，一个是通过PC浏览器访问的Web端。

### 桌面应用端

*   传统的软件端操作界面，可以对服务器的站点进行高效的管理
*   高效的操作管理，可快速搭建站点、数据库、FTP等服务
    ![](https://www.bt.cn/Public/images/win_pc.png)

### Web应用端

*   相对于桌面应用端有更好的体验，跨终端、跨平台
*   高效的操作管理，可快速搭建站点、数据库、FTP等服务
*   完善的在线文件管理器，轻松实现图片查看，文本编辑，文件打包解压
    ![](https://www.bt.cn/Public/images/win_web.png)
    

> Web端的功能更为全面，只要SQLServer的安装需要使用客户端，其他的都可以在Web端完成，因此后续的指南我们均以Web端作为范例来进行具体说明。
