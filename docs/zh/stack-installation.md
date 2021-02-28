# 初始化安装

在云服务器上部署 BT 预装包之后，请参考下面的步骤快速入门。

> 宝塔 Linux 面板和宝塔 Windows 面板有一定的功能差异，后续文档会在必要的时候做出说明。

## 准备

1. 在云控制台获取您的 **服务器公网IP地址** 
2. 在云控制台安全组中，检查 **Inbound（入）规则** 下的 **TCP:8888** 端口是否开启
3. 若想用域名访问 BT，请先到 **域名控制台** 完成一个域名解析

## 登录

BT 部署到你的服务器后，即可开始使用：

1. 使用 Chrome 或 Firefox 浏览器访问：*http://服务器公网IP:8888* ，进入登录页面（[打不开？](#常见问题)）  
   ![BT 登录界面](https://libs.websoft9.com/Websoft9/DocsPicture/zh/btlinux/bt-login-websoft9.png)

2. 输入默认账号密码（[不知道密码？](/zh/stack-accounts.md#bt)），进入宝塔后台
   ![BT 后台界面](https://libs.websoft9.com/Websoft9/DocsPicture/zh/btlinux/bt-console-websoft9.png)

3. 如果出现下面的绑定宝塔账号提示，访问：*http://服务器公网IP:8888/soft* 即可绕开
   ![BT 后台界面](https://libs.websoft9.com/Websoft9/DocsPicture/zh/btwin/bt-registerneed-websoft9.png)

  > 绑定宝塔官方账号不是必须的步骤

## 升级

在使用宝塔之前，建议首先检查升级，保证系统为最新状态  

![宝塔升级](https://libs.websoft9.com/Websoft9/DocsPicture/zh/btlinux/bt-update001-websoft9.png)

## 搭建环境

升级完成后，就可以开始使用宝塔搭建你所需的环境。

### 安装推荐套件

宝塔默认会推荐一个组合的安装套件，如果套件合适你的需求，可以安装它：

1. 确定所需的套件，在套件界面上选择组件版本，例如：PHP7.4, MySQL 5.6
![](http://libs.websoft9.com/Websoft9/DocsPicture/zh/btlinux/bt02.png)

2. 组件选择完成后，点击【一键安装】，耐心等待安装直至结束
![](http://libs.websoft9.com/Websoft9/DocsPicture/zh/btlinux/bt03.png) 


### 安装更多软件

初始化安装之外的安装，都可以通过【软件商店（管理）】去安装更多的组件。

* 宝塔 Linux 面板之【软件商店】
  ![宝塔 Linux 软件商店](http://libs.websoft9.com/Websoft9/DocsPicture/zh/btlinux/bt-linuxapps-websoft9.png) 

* 宝塔 Windows 面板之【软件管理】
  ![宝塔 Windows 软件管理](http://libs.websoft9.com/Websoft9/DocsPicture/zh/btwin/bt-winapps-websoft9.png) 

**示例1 安装Tomcat：** 打开宝塔【软件管理】>【运行环境】>【Tomcat】，点击【安装】即可  

**示例1 安装Node.js：** 打开宝塔【软件管理】>【运行环境】>【PM2管理器】，点击【安装】即可

## 常见问题

#### 浏览器访问 *http://服务器公网IP：8888* 没有内容（白屏没有结果）？

您的服务器对应的安全组 8888 端口没有开启（入规则），导致浏览器无法访问到服务器的任何内容。

#### 8888 端口成功开启仍然无法访问？

可能您安装了旧版本（低于宝塔Windows版 V6.9），需参考[旧版本 Windows 面板初始化指南](/zh/win/stack-installation.md)

#### 能否将 PHP, Java 和 Node.js 安装到一起？

可以。虽然宝塔可选的组件很多，但请把握一个原则："不用的不装，什么时候用什么时候装"。

#### 需要运行 PHP 网站怎么安装环境？

安装推荐套餐，即安装：Apache，MySQL，PHP， phpMyAdmin 等

#### 安装哪个 PHP 版本合适？

根据你的应用决定 PHP 版本，如果应用没有明确所需的版本，建议安装 PHP7.2 或以上版本。另外，除非有多版本需求，请不要主动安装多个PHP版本

#### 有哪些软件是必须安装的吗？

没有必须安装的软件，请根据应用要求去安装。原则："不用的不装，什么时候用什么时候装"。

#### 宝塔 Windows 面板中 SQLServer 怎么安装？

建议自行下载 Microsoft 官方的包进行安装。

#### IIS 与 Apache，Nginx 可以同时安装吗？

三者选其一，否则会引起不必要的软件冲突

#### 宝塔 Windows 面板究竟安装那个 Web 服务器呢？

推荐使用 IIS
