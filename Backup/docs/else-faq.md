# FAQ

#### aaPanel support multi-language?

aaPanel have two edition: English and Chinese, your can only install one edition every time

#### What is the default character set?

UTF-8

#### Can I use the RDS of Cloud Provider for application on aaPanel?

Yes

#### Where is the database connection configuration of aaPanel?

Database configuration information in *LocalSettings.php* in the [aaPanel installation directory](/stack-components.md#mysql)

#### If there is no domain name, can I deploy aaPanel?

Yes, visit aaPanel by *http://Internet IP:8888*


#### Is it possible to modify the source path of aaPanel?

No

#### Can I configure this aaPanel if I don't understand the Linux command?

Yes, you can use GUI of aaPanel, no commands

#### How to change the permissions of filesytem?

Change owner(group) or permissions like below:

```shell

#e.g. user is apache
chown -R apache.apache /data/wwwroot

#e.g. user is nginx
chown -R nginx.nginx /data/wwwroot

#modify the read/modify/excuse permissions

find /data/wwwroot -type d -exec chmod 750 {} \;
find /data/wwwroot -type f -exec chmod 640 {} \;
```

#### What's the difference between Deployment and Installation?

- Deployment is a process of installing and configuring a sequence of software in sequence in a different order, which is a complex system engineering.  
- Installation is the process of starting the initial wizard after the application is prepared.  
- Installation is simpler than deployment. 

#### What's Cloud Platform?

Cloud platform refers to platform manufacturers that provide cloud computing services, such as: **Azure, AWS, Alibaba Cloud, HUAWEI CLOUD, Tencent Cloud**, etc.

#### What is the difference between Instance, Cloud Server, Virtual Machine, ECS, EC2, CVM, and VM?

No difference, just the terminology used by different manufacturers, actually cloud servers