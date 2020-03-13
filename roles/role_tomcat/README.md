Ansible Role: Tomcat
=========

本 Role 用于在 CentOS Ubuntu AmazonLinx 安装 Tomcat。
## Requirements

运行本 Role，请确认符合如下的必要条件：

| **Items**      | **Details** |
| ------------------| ------------------|
| Operating system | CentOS7.x， Ubuntu， AmazonLinux |
| Python 版本 | Python2  |
| Python 组件 |    |
| Runtime |  |


## Related roles

本 Role 在语法依赖role_jdk，但程序运行时需要确保已经运行：common Role，和jdk role 局里说明：：

```
roles:
    - {role: role_common, tags: "role_common"}
    - {role: role_jdk, tags: "role_jdk"}
    - {role: role_tomcat, tags: "role_tomcat"}
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
    - {role: role_tomcat, tags: "role_tomcat"}
```

## FAQ
