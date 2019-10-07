---
layout: post
title: SSH远程阿里云服务器出现"Permission denied (publickey)"报错的解决办法
author: suxinde2009
category: Alibaba-ECS
date: 2019-10-07
---

### 问题
ssh远程阿里云服务器时，出现"ermission denied (publickey)"报错

### 解决

通过阿里云服务端控制台远程服务器，修改配置文件可以解决。

~~~
vim /etc/ssh/sshd_config 将PasswordAuthentication的参数设置为yes 应该在文件末尾    
systemctl restart sshd.service 重启ssh服务
systemctl status sshd.service 查看ssh服务状态
~~~

### 参考

[Mac终端连接阿里云服务器出现Permission denied (publickey)](https://blog.csdn.net/Axela30W/article/details/81940557)
