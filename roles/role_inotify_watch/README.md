Ansible Role: inotify_watch
=========

本 Role 用于 PHP 环境下对文件进行自动权限管理。
## Requirements

运行本 Role，请确认符合如下的必要条件：

| **Items**      | **Details** |
| ------------------| ------------------|
| Operating system | CentOS7.x |
| Python 版本 | Python2  |
| Python 组件 |    |
| Runtime |  Apache 或 Nginx|


## Related roles

本 Role 在语法不依赖其他 role 的变量，但程序运行时需要确保已经运行： apache 或 nginx Role。以 LAMP 为例：

```
roles:
    - {role: role_apache, tags: "role_apache"}
    - {role: role_mysql, tags: "role_mysql"}
    - {role: role_php-fpm, tags: "role_php-fpm"}
    - {role: role_lamp, tags: "role_lamp"}
    - {role: role_inotify_watch, tags: "inotify_watch"}
```


## Variables

暂无

## Example

```
- name: LAMP
  hosts: all
  become: yes
  become_method: sudo 
  vars_files:
    - vars/main.yml 
  
  vars:
    phpmyadmin_webs: 'apache'
    phpmyadmin_mysql_password: '123456'
    phpmyadmin_php_version: '7.2'

    - {role: role_common, tags: "role_common"}
    - {role: role_cloud, tags: "role_cloud"}
    - {role: role_apache, tags: "role_apache"}
    - {role: role_redis, tags: "role_redis"}
    - {role: role_mysql, tags: "role_mysql"}
    - {role: role_php-fpm, tags: "role_php-fpm"}
    - {role: role_lamp, tags: "role_lamp"}
    - {role: role_phpmyadmin, tags: "role_phpmyadmin"}
    - {role: role_9panel, tags: "role_9panel"}
    - {role: role_inotify_watch, tags: "inotify_watch"}
    - {role: role_init_password, tags: "init_password"}
    - {role: role_preend, tags: "role_preend"}
    - {role: role_end, tags: "role_end"}
```

## FAQ
