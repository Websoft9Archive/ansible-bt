# 旧版本 Windows 面板初始化指南

以下内容适用于 Windows 宝塔面板 V6.9 以下的版本：

## 准备

1. 在云控制台获取您的 **服务器公网IP地址** 
2. 在云控制台安全组中，检查 **Inbound（入）规则** 下的 **TCP:888** 端口是否开启
3. 若想用域名访问 BT，请先到 **域名控制台** 完成一个域名解析

## Web 后台初始化

默认不能访问 Web 端（[桌面端和 Web 后台](/zh/win/stack-installation.md#桌面端和web端)），需远程到服务器，完成进行**初始化设置**后方可。

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

## 桌面端和Web端

宝塔 Windows 面板有两个访问端口：一个是服务器的桌面端，一个是通过PC浏览器访问的Web端。

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
