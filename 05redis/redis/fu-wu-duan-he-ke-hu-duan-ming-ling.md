# 学习目标 {#学习目标}

* 了解Redis服务器端和客户端的命令

  # 服务器端 {#服务器端}

* 服务器端的命令为redis-server

* 可以使用help查看帮助⽂档

  > redis-server --help

* 个人习惯
  > ps aux \| grep redis 查看redis服务器进程  
  > sudo kill -9 pid 杀死redis服务器  
  > sudo redis-server /etc/redis/redis.conf 指定加载的配置文件

# 客户端 {#客户端}

* 客户端的命令为redis-cli
* 可以使用help查看帮助⽂档
  > redis-cli --help
* 连接redis

  > redis-cli

  ![](/assets/连接redis.png)

* 运行测试命令

  > ping

  ![](/assets/redis测试连接.png)

* 切换数据库

* 数据库没有名称，默认有16个，通过0-15来标识，连接redis默认选择第一个数据库

  > select 10

  ![](/assets/redis选择数据库.png)



