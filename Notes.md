# BT Notes

宝塔安装必须准备一个非常干净的环境，因此 role_common 在 bt role 之后运行

## 随机密码

通过宝塔自带的修改密码脚本 tools.py 实现随机密码

```
init_application:
  bt:
    username: administrator
    password: 123456
    service_before: bt.service
    commands:
      - sudo su
      - cd /www/server/panel
      - python tools.py panel $new_password
```
