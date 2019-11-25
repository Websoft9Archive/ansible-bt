# 更新升级

网站技术日新月异，**更新升级**是维护工作之一，长时间不升级的程序，就如长时间不维护的建筑物一样，会加速老化、功能逐渐缺失直至无法使用。  

这里注意更新与升级这两词的差异（[延伸阅读](https://support.websoft9.com/docs/faq/zh/tech-upgrade.html#更新-vs-升级)），例如：  

- 操作系统打个补丁常称之为**更新**，Ubuntu16.04 变更为 Ubuntu18.04，称之为**升级**
- MySQL5.6.25-->MySQL5.6.30 常称之为**更新**，MySQL5.6->MySQL5.7 称之为**升级**

BT 完整的更新升级包括：系统级更新（操作系统和运行环境）和 BT 程序升级两种类型

## 系统级更新

### Linux 系统

针对 Linux 系统，使用 SSH 登录后，运行一条更新命令，即可完成系统级更新：

``` shell
#For Ubuntu&Debian
apt update && apt upgrade -y

#For Centos&Redhat
yum update -y
```
> 本部署包已预配置一个用于自动更新的计划任务。如果希望去掉自动更新，请删除对应的Cron

### Window 系统

Windows服务器的更新与本地电脑类似，手动找到更新管理程序，设置自动下载自动更新即可。


## 宝塔升级

### 宝塔内核升级

宝塔提供了一键在线升级功能，只要根据系统提示，点击升级按钮即可完成升级

![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/btlinux/bt-update001-websoft9.png)

### 环境组件升级

宝塔在使用中一般会安装大量的软件或组件，包括：php，mysql，phpmyadmin等，

![](http://libs.websoft9.com/Websoft9/DocsPicture/zh/btwin/bt-win-intallhj-websoft9.png)

升级请参考官方教程《[宝塔-软件管理](https://www.kancloud.cn/chudong/bt2017/424281)》