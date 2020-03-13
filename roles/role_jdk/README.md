Ansible Role: JDK
=========

本 Role 用于在 CentOS Ubuntu AmazonLinx 安装 JDK。
## Requirements

运行本 Role，请确认符合如下的必要条件：

| **Items**      | **Details** |
| ------------------| ------------------|
| Operating system | CentOS7.x， Ubuntu， AmazonLinux |
| Python 版本 | Python2  |
| Python 组件 |    |
| Runtime |  |


## Related roles

本 Role 在语法不依赖其他 role 的变量，但程序运行时需要确保已经运行：common Role， 局里说明：：

```
roles:
    - {role: role_common, tags: "role_common"}
    - {role: role_jdk, tags: "role_jdk"}
```

## Variables

暂无

## Example

```
- name: example
  hosts: all
  become: yes
  become_method: sudo 
  vars_files:
    - vars/main.yml 
  
  role:
    - {role: role_common, tags: "role_common"}
    - {role: role_jdk, tags: "role_jdk"}
```

## FAQ
