# 安全通知


#### IIS解析漏洞告警及处理方案

云鼎实验室在日常安全运营中发现，宝塔 Windows 面板默认安装的 IIS+PHP 环境存在 IIS 解析漏洞，攻击者可以在任意文件上传点上传一个包含着恶意 PHP 代码的文件（图片、TXT、压缩包等）后，通过利用 IIS 解析漏洞即可执行 PHP 代码，可能会导致用户代码、数据库泄露。

如果您通过宝塔安装了IIS，就会产生一个IIS的解析漏洞，您需要做出如下修改：

1.修改由IIS在根目录中自动生成“web.config”的文件（路径：“C:\inetpub\wwwroot”），将“resourceType”对应的"Unspecified"修改为“File”。
2.如果您新建了网站中包含了web.config文件，也需要做出上述修改

..............................................................

如果安装了IIS，又安装了PHP，您需要修改如下配置：

1. 打开“C:\Windows\System32\inetsrv\config\applicationHost.config”文件
2. 将“<add name="PHP_FastCGI" path="*.php" verb="*" modules="FastCgiModule" scriptProcessor="C:\BtSoft\WebSoft\php\5.4\php-cgi.exe" resourceType="Unspecified" />”中“resourceType”对应的"Unspecified"修改为“File”。

以上路径以PHP5.4为例，如果安装了多个php版本，每个PHP目录均需要进行修改