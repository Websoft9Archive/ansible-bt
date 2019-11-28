# 参数

BT 预装包包含 BT 运行所需一序列支撑软件（简称为“组件”），下面列出主要组件名称、安装路径、配置文件地址、端口、版本等重要的信息。

## 路径

### Linux 版

*   安装目录：*/www/server*
*   网站目录：*/www/wwwroot/default*
*   Apache目录：*/www/server/httpd*
*   Nginx目录：*/www/server/nginx*
*   MySQL目录：*/www/server/mysql*
*   PHP目录：*/www/server/php*
*   Redis目录：*/www/server/redis*
*   Memcached目录：/usr/local/memcached*
*   日志目录：*/www/wwwlogs*

访问方式：Web面板

### Windows 版

*   安装目录：*C:\BtSoft\ServerAdmin*
*   网站目录：*C:\wwwroot*
*   MySQL目录：*C:\BtSoft\WebSoft\mysql*
*   日志文件：*C:\BtSoft\WebSoft\apache\logs*

访问方式：Web面板 或 服务器客户端

## 端口号

在云服务器中，通过 **[安全组设置](https://support.websoft9.com/docs/faq/zh/tech-instance.html)** 来控制（开启或关闭）端口是否可以被外部访问。 

本应用建议开启的端口如下：

| 名称 | 端口号 | 用途 |  必要性 |
| --- | --- | --- | --- |
| HTTP | 80 | 通过 HTTP 访问你的网站 | 必须 |
| HTTPS | 443 | 通过 HTTPS 访问你的网站 | 可选 |
| BT| 8888 | 访问 宝塔 Linux 版的管理界面 | 必须 |
| BT | 888 | 访问 宝塔 Windows 版的管理界面 | 必须 |
| MySQL | 3306 | 远程连接 MySQL | 可选 |

## 版本号

组件版本号可以宝塔控制台查看