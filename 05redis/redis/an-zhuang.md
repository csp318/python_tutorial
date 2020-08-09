# Redis 安装

* 当前redis最新稳定版本是4.0.9
* 当前ubuntu虚拟机中已经安装好了redis，以下步骤可以跳过 最新稳定版本下载链接：
  [http://download.redis.io/releases/redis-4.0.9.tar.gz](http://download.redis.io/releases/redis-4.0.9.tar.gz)
* step1:下载

  > wget [http://download.redis.io/releases/redis-4.0.9.tar.gz](http://download.redis.io/releases/redis-4.0.9.tar.gz)

  ![](/assets/下载redis.png)

* step2:解压

  > tar xzf redis-4.0.9.tar.gz

* step3:移动，放到usr/local目录下

  > sudo mv ./redis-4.0.9 /usr/local/redis/

* step4:进入redis目录

  > cd /usr/local/redis/

* step5:生成

  > sudo make

  ![](/assets/redismake.png)

* step6:测试,这段运行时间会较长

  > sudo make test

  ![](/assets/maketest.png)

* step7:安装,将redis的命令安装到/usr/local/bin/目录

  > sudo make install

* step8:安装完成后，我们进入目录/usr/local/bin中查看

  > cd /usr/local/bin  
  > ls -all

  ![](/assets/p1_12.png)

  > * redis-server redis服务器
  > * redis-cli redis命令行客户端
  > * redis-benchmark redis性能测试工具
  > * redis-check-aof AOF文件修复工具
  > * redis-check-rdb RDB文件检索工具

* step9:配置文件，移动到/etc/目录下

* 配置文件目录为/usr/local/redis/redis.conf

  > sudo cp /usr/local/redis/redis.conf /etc/redis/

* Mac 上安装 Redis:

  * 安装 Homebrew：

  > [https://brew.sh/](https://brew.sh/)

  * 使用 brew 安装 Redis

  > [https://www.cnblogs.com/cloudshadow/p/mac\_brew\_install\_redis.html](https://www.cnblogs.com/cloudshadow/p/mac_brew_install_redis.html)



