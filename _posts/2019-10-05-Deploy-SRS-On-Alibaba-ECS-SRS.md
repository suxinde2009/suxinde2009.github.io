---
layout: post
title: 阿里云部署SRS流媒体服务器接收rtmp出现 tcp://XX.xx.xx.xx:1935 Connection time out
author: suxinde2009
category: SRS
date: 2019-10-05
---

在阿里的ECS服务器上搭建SRS流媒体服务器时，遇到tcp建立不了连接的问题。
报错形如：

~~~
[rtmp @ XXXXx] Cannot open connection tcp://xx.xx.xx.xx:1935
rtmp://xx.xx.xx.xx/live/123/livestream: Operation timed out
~~~


### 原因
ECS实例安全组的问题，阿里云的ECS实例安全组相当于防火墙，由于安全组没有开放1935端口（流媒体推流端口）

### 解决
在安全组中开放1935端口即可