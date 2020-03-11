# 更多...

下面每一个方案，都经过实践证明行之有效，希望能够对你有帮助

## 域名绑定

绑定域名的前置条件是：已经完成域名解析（登录域名控制台，增加一个A记录指向服务器公网IP）  

完成域名解析后，从服务器安全和后续维护考量，需要完成**域名绑定**：

BT 域名绑定操作步骤：

![](http://libs.websoft9.com/Websoft9/DocsPicture/en/bt/bt-setdns-websoft9.png)


## 如何找回BT后台密码?

如果是忘记了密码，请使用WinSCP或Putty运行如下命令，重置密码
~~~

//示例：将admin用户的密码重置为admin123

cd /www/server/panel && python tools.pyc panel admin123 admin

//如果提示多次登录失败，暂时禁止登录 请输入以下命令，清除登录限制
rm -f /www/server/panel/data/*.login

~~~