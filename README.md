### 该仓库作为ansible-playbook模板使用

*目录结构说明:*

.github 用于存放 GitHub Actions 配置
   
docs 用于存放文档
   
  
roles 用于存放role目录
   
vars 存放变量

   
ansible.cfg 项目配置
 > 注意: 由于在Centos7中YUM/Dnf 等包管理工具没有获得python3模块的支持 interpreter_python需要指定python2为解析器;Ubuntu18.04/Centos8指定使用Python3作为解析器,如果项目需要考虑Ubuntu18.04和Centos7,优先将解析器设置为python2;目前发现 docker_compose modules 需要python3,如果多系统支持 docker_compose modules 考虑使用 shell modules实现
    
main.yml Playbook入口
   
requirements.yml  依赖文件,存放所需role仓库地址
 > 将项目需要的 role 仓库地址写入该文件



*注意:*

roles 目录内模块化的role保持默认 role_xxx的命名,该项目所需要的编写的role 直接以项目名称命名以示区分