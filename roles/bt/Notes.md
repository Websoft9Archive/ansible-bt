## 安装注意

官方安装方案解读：BT 官方提供了 shell 的完全自动化过程，一条命令跑完。BT 官方要求纯净的操作系统，BT 所学的一切依赖组件，都由 BT 的自动化脚本安装完成。  
我们的公共 common roles 会安装一些依赖组件，反而导致 BT 官方脚本出现版本冲突而报错，终止 Ansible，所以公共 common roles 不可包含到 ansible-bt 中。   

经过集体探讨，方案如下：

1. 只使用 cloud,  end 两个公共roles
2. 新增的 bt roles 主要用于修改 BT 的默认管理员账号密码、关闭加密访问链接。
