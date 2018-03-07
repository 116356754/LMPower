## 电能采集报表总体结构

采集和报表现在是分成两个部分：采集服务是node.js编写的程序，需要借助其他NSSM实现安装服务的功能；报表服务是java编写的程序，需要借助tomcat实现安装服务；

程序存储的数据库目前采用的是mysql 5.7.X版本来存储实时或者历史数据的，同时需要借助Navicat for mysql 工具来实现导入数据库的功能；

客户端是采用C\#来开发的，需要安装.net 4.0 framework;

总体而言有如下四个部分组成：

![](/assets/folders.png)

