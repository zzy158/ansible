# ansible 

1. ansible 安装

2. ansible 基本语法

   * ansible -i 清单文件 主机名 -m 模版  -a 命令        直接引用某个模版文件
   * ansible-playbook *.yaml    执行剧本文件
   * ansible all -m setup 查看所有变量文件     变量文件

3. ansible yaml

   * 基本格式

     ![](D:\zzygit\picture\shili01.jpg)

4. roles

* roles 是ansible playbook 模块化的一种模式  方便代码复用

* 目录结构  

  1. templates    模版文件   此文件是用jinja2模版用变量来写 

  2. tasks    创建后 需要用到的模块  

  3. handlers   特定条件下触发的任务 一般用于服务重启

  4. vars 编写变量  键值对形式 

  5. meta 存放元数据

  6. default 默认变量 优先级小于 vars

  7. files 存放文档  可以是.sql  .index 等静态的文件  

     