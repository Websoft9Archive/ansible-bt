# Parameters

The aaPanel deployment package contains a sequence software (referred to as "components") required for aaPanel to run. The important information such as the component name, installation directory path, configuration file path, port, version, etc. are listed below.

## Path

### aaPanel

aaPanel installation directory: */www/server*  
aaPanel site default directory: */www/wwwroot*    
aaPanel logs file：*tmp/panelBoot*     
aaPanel site logs file：*/www/wwwlogs*  

### PHP

PHP configuration file: */www/server/php/{52|53|54|55|56|70|71}/etc/php.ini*  
PHP installation directory: */www/server/php*

### Apache

Apache vhost configuration file：*/www/server/panel/vhost/apache*  
Apache main configuration file：*/www/server/apache/conf/httpd.conf*  

### Nginx

Nginx vhost configuration file：*/www/server/panel/vhost/nginx*  
Nginx main configuration file：*/www/server/nginx/conf/nginx.conf*  

### MySQL

MySQL installation directory: */www/server/mysql*  
MySQL data directory: */www/server/data*  
MySQL configuration file: */etc/my.cnf*    
phpmyadmin installation directory: */www/server/phpmyadmin*   

## Resis

Redis installation directory: */www/server/redis*

## Memcached

Memcached installation directory */www/server//usr/local/memcached*

## Ports

You can control(open or shut down) ports by **[Security Group Setting](https://support.websoft9.com/docs/faq/tech-instance.html)** of your Cloud Server whether the port can be accessed from Internet.

These ports should be opened for this application:

| Name | Number | Use |  Necessity |
| --- | --- | --- | --- |
| MySQL | 3306 | Remote connect MySQL | Optional |
| HTTP | 80 | HTTP requests for aaPanel | Required |
| HTTPS | 443 | HTTPS requests aaPanel | Optional |

## Version

You can see the version from aaPanel or running these commands

```shell
# Linux Version
lsb_release -a

# PHP Version
php -v

# List Installed PHP Modules
php -m

# Apache version on Ubuntu
apache2 -v

# Apache version on Centos
httpd -v

# List Installed Apache Modules
apachectl -M

# MySQL version:
mysql -V
```