># 关系型数据库
>>## 安装数据库及去其它软件
  >>### 更新源
   >>>- 1.用vim打开源列表文件:sudo vim /etc/apt/sources.list
   >>>- 2.将下面的源粘贴到源列表里。  
   
    deb http://mirrors.aliyun.com/ubuntu/ xenial main restricted universe multiverse
    deb http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted universe multiverse
    deb http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted universe multiverse
    deb http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse
    ##测试版源
    deb http://mirrors.aliyun.com/ubuntu/ xenial-proposed main restricted universe multiverse
    # 源码
    deb-src http://mirrors.aliyun.com/ubuntu/ xenial main restricted universe multiverse
    deb-src http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted universe multiverse
    deb-src http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted universe multiverse
    deb-src http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse
    ##测试版源
    deb-src http://mirrors.aliyun.com/ubuntu/ xenial-proposed main restricted universe multiverse
    # Canonical 合作伙伴和附加
    deb http://archive.canonical.com/ubuntu/ xenial partner
    deb http://extras.ubuntu.com/ubuntu/ xenial main  
    
   >>### 安装 mysql
      1.sudo apt-get update:更新源
      2.sudo apt-get install mysql-client mysql-server:安装mysql服务器和客户端
      3.sudo /etc/init.d/mysqld start:启动mysql服务
   >>### 安装 Apach（一种服务器）
      1.sudo apt-get update
      2.sudo apt-get install tasksel
      3.sudo tasksel
   >>### 安装 Workbench（数据库可视化界面）
      1. sudo apt-get install mysql-workbench
  >>## MySQL 命令行操作
     1.连接到本机上的MYSQL:mysql -u root -p,直接回车即可进入到MYSQL中了，MYSQL的提示符是： mysql>
     2.退出MYSQL命令： exit （回车）
     3.创建数据库：create database <数据库名>
