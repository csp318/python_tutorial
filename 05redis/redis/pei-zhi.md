# 学习目标 {#学习目标}

* 能够根据参考资料修改常用Redis配置

# 配置 {#配置}

* Redis的配置信息在/etc/redis/redis.conf下。

* 查看

  > sudo vi /etc/redis/redis.conf

# 核心配置选项 {#核心配置选项}

* 绑定ip：如果需要远程访问，可将此行注释，或绑定多个真实ip
  > bind 127.0.0.1
* 端口，默认为6379
  > port 6379
* 是否以守护进程运行

  * 如果以守护进程运行，则不会在命令行阻塞，类似于服务
  * 如果以非守护进程运行，则当前终端被阻塞
  * 设置为yes表示守护进程，设置为no表示⾮守护进程
  * 推荐设置为yes

  > daemonize yes

* 数据文件

  > dbfilename dump.rdb

* 数据文件件存储路径
  > dir /var/lib/redis
* 日志文件
  > logfile "/var/log/redis/redis-server.log"
* 数据库，默认有16个
  > database 16
* 主从复制，类似于双机备份。
  > slaveof

# 参考资料 {#参考资料}

redis配置信息[http://blog.csdn.net/ljphilp/article/details/52934933](http://blog.csdn.net/ljphilp/article/details/52934933)

