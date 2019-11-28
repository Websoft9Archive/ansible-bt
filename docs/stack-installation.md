# Initial Installation

If you have completed the aaPanel deployment on Cloud Platform, the following steps is for you to start use it quikly

## Preparation

1. Get the **Internet IP** on your Cloud Platform
2. Check you **[Inbound of Security Group Rule](https://support.websoft9.com/docs/faq/tech-instance.html)** of Cloud Console to ensure the TCP:8888 is allowed
3. Make a domain resolution on your DNS Console if you want to use domain for aaPanel

## aaPanel environment setup

Using local Chrome or Firefox to visit the URL *http://Internet IP:8888*, go to the login page of aaPanel

![](https://libs.websoft9.com/Websoft9/DocsPicture/en/bt/bt-login-websoft9.png)

### Upgrade

First, you should upgrade aaPanel to latest version  

![](https://libs.websoft9.com/Websoft9/DocsPicture/en/bt/bt-update001-websoft9.png)

### Setup PHP runtime

Start to setup LAMP or LNMP according the aaPanel's remainder

1. 其中的每个组件版本可选（如下图LAMP主流版本选择）：
![](https://libs.websoft9.com/Websoft9/DocsPicture/en/bt/bt-installlamp-websoft9.png)

2. 参完成选择后，点击“一键安装”，待安装完成后您就可以配置自己的网站了。
![](https://libs.websoft9.com/Websoft9/DocsPicture/en/bt/bt-installlamping-websoft9.png) 


### Setup more

初始化安装之外的安装，都可以通过【软件管理】去安装更多的组件。

![](https://libs.websoft9.com/Websoft9/DocsPicture/en/bt/bt-appstore-websoft9.png)

> More useful aaPanel guide, please refer to [aaPanel forum](https://forum.aapanel.com/)

## Q&A

#### I can't visit the start page of aaPanel?

Your TCP:8888 of Security Group Rules is not allowed so there no response from Chrome or Firefox

#### 能否将 PHP, Java 和 Node.js 安装到一起？

可以，但不建议。虽然宝塔的功能强大，能够安装的组件足够多，但是请把握一个原则，能不装的不要装，现在用不到的不要装
