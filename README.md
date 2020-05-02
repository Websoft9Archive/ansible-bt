
# BT（宝塔） 自动化安装与部署

本项目是由 [Websoft9](https://www.websoft9.com) 研发的 [宝塔](https://www.bt.cn/) 自动化安装程序，开发语言是 Ansible。使用本项目，只需要用户在 Linux 上运行一条命令，即可自动化安装BT，让原本复杂的安装过程变得没有任何技术门槛。  

本项目是开源项目，采用 LGPL3.0 开源协议。

## 配置要求

安装本项目，确保符合如下的条件：

| 条件       | 详情       | 备注  |
| ------------ | ------------ | ----- |
| 操作系统       | CentOS7.x, Ubuntu18.04, Amazon Linux2       |    |
| 公有云| AWS, Azure, 阿里云, 华为云, 腾讯云 |  |
| 私有云|  KVM, VMware, VirtualBox, OpenStack |  |
| 服务器配置 | 最低1核1G，安装时所需的带宽不低于10M |  建议采用按量100M带宽 |

## 组件

包含的核心组件为：宝塔面板

更多请见[参数表](/docs/zh/stack-components.md)

## 本项目安装的是宝塔最新版吗？

本项目是下载 [BT官方脚本](https://www.bt.cn/download/linux.html) 安装。 

如需安装最新版本，请修改 bt role的变量文件 [main.yml](/roles/bt/defaults/main.yml) 中相关的下载地址

```
bt_download_url:
  RedHat:
    zh: http://download.bt.cn/install/install_6.0.sh
    en: http://download.bt.cn/install/install_6.0_en.sh 
  Debian:
    zh: http://download.bt.cn/install/install-ubuntu_6.0.sh
    en: http://download.bt.cn/install/install-ubuntu_6.0_en.sh
```

我们会定期检查版本准确性，并增加官方最新的stable版本，以保证用户可以顺利安装所需的宝塔版本。

## 安装指南

以 root 用户登录 Linux，运行下面的**一键自动化安装命令**即可启动自动化部署。若没有 root 用户，请以其他用户登录 Linux 后运行 `sudo su -` 命令提升为 root 权限，然后再运行下面的脚本。

```
wget -N https://raw.githubusercontent.com/Websoft9/ansible-linux/master/scripts/install.sh; bash install.sh -r bt
```

脚本后启动，就开始了自动化安装，必要时需要用户做出交互式选择，然后耐心等待直至安装成功。

**安装中的注意事项：**  

1. 操作不慎或网络发生变化，可能会导致SSH连接被中断，安装就会失败，此时请重新安装
2. 安装缓慢、停滞不前或无故中断，主要是网络不通（或网速太慢）导致的下载问题，此时请重新安装

多种原因导致无法顺利安装，请使用我们在公有云上发布的 [BT 镜像](https://apps.websoft9.com/bt) 的部署方式


## 文档

文档链接：https://support.websoft9.com/docs/bt/zh

## FAQ

- 命令脚本部署与镜像部署有什么区别？请参考：[镜像部署-vs-脚本部署](https://support.websoft9.com/docs/faq/zh/bz-product.html#镜像部署-vs-脚本部署)
- 本项目支持在 Ansible Tower 上运行吗？支持
