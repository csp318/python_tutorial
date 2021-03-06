# 学习目标 {#目标}

* 能够描述出什么是 nosql 
* 能够说出 Redis 的特点

# nosql介绍 {#nosql介绍}

## NoSQL：一类新出现的数据库\(not only sql\)

* 泛指非关系型的数据库
* 不支持SQL语法
* 存储结构跟传统关系型数据库中的那种关系表完全不同，nosql中存储的数据都是KV形式
* NoSQL的世界中没有一种通用的语言，每种nosql数据库都有自己的api和语法，以及擅长的业务场景
* NoSQL中的产品种类相当多：
  * Mongodb
  * Redis
  * Hbase hadoop
  * Cassandra hadoop

## NoSQL和SQL数据库的比较： {#nosql和sql数据库的比较：}

* 适用场景不同：sql数据库适合用于关系特别复杂的数据查询场景，nosql反之
* “事务”特性的支持：sql对事务的支持非常完善，而nosql基本不支持事务
* 两者在不断地取长补短，呈现融合趋势

# Redis简介 {#redis简介}

* Redis是一个开源的使用ANSI C语言编写、支持网络、可基于内存亦可持久化的日志型、Key-Value数据库，并提供多种语言的API。从2010年3月15日起，Redis的开发工作由VMware主持。从2013年5月开始，Redis的开发由Pivotal赞助。
* Redis是 NoSQL技术阵营中的一员，它通过多种键值数据类型来适应不同场景下的存储需求，借助一些高层级的接口使用其可以胜任，如缓存、队列系统的不同角色

# Redis特性 {#redis特性}

* Redis 与其他 key - value 缓存产品有以下三个特点：
* Redis支持数据的持久化，可以将内存中的数据保存在磁盘中，重启的时候可以再次加载进行使用。
* Redis不仅仅支持简单的key-value类型的数据，同时还提供list，set，zset，hash等数据结构的存储。
* Redis支持数据的备份，即master-slave模式的数据备份。

# Redis 优势 {#redis-优势}

* 性能极高 – Redis能读的速度是110000次/s,写的速度是81000次/s 。
* 丰富的数据类型 – Redis支持二进制案例的 Strings, Lists, Hashes, Sets 及 Ordered Sets 数据类型操作。
* 原子 – Redis的所有操作都是原子性的，同时Redis还支持对几个操作全并后的原子性执行。
* 丰富的特性 – Redis还支持 publish/subscribe, 通知, key 过期等等特性。

# Redis应用场景 {#redis应用场景}

* 用来做缓存\(ehcache/memcached\)——redis的所有数据是放在内存中的（内存数据库）
* 可以在某些特定应用场景下替代传统数据库——比如社交类的应用
* 在一些大型系统中，巧妙地实现一些特定的功能：session共享、购物车
* 只要你有丰富的想象力，redis可以用在可以给你无限的惊喜…….

# 推荐阅读 {#推荐阅读}

* [redis官方网站](https://redis.io/)
* [redis中文官网](http://redis.cn/)



