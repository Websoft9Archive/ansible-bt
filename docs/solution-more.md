# More

Each of the following solutions has been proven to be effective and we hope to be helpful to you.

## Domain binding

The precondition for **Domain binding** is have completed the **Domain resolution** for aaPanel Instance.

From the perspective of server security and subsequent maintenance considerations, the **Domain Binding** step cannot be omitted.

aaPanel domain name binding steps:

1. Login to aaPanel
2. Set DNS  
   ![](http://libs.websoft9.com/Websoft9/DocsPicture/en/bt/bt-setdns-websoft9.png)

## Rest aaPanel's password

如果是忘记了密码，请使用WinSCP或Putty运行如下命令，重置密码
~~~

//Change control Panel login password，e.g. 123456

cd /www/server/panel && python tools.py panel 123456

~~~