# StrictRedis对象用法 {#strictredis对象⽅法}

* 通过init创建对象，指定参数host、port与指定的服务器和端口连接，host默认为localhost，port默认为6379，db默认为0

```
sr = StrictRedis(host='localhost', port=6379, db=0)

简写
sr=StrictRedis()
```

* 根据不同的类型，拥有不同的实例方法可以调用，与前面学的redis命令对应，方法需要的参数与命令的参数一致

## string {#string}

* set
* setex
* mset
* append
* get
* mget
* key

## keys {#keys}

* exists
* type
* delete
* expire
* getrange
* ttl

## hash {#hash}

* hset
* hmset
* hkeys
* hget
* hmget
* hvals
* hdel

## list {#list}

* lpush
* rpush
* linsert
* lrange
* lset
* lrem

## set {#set}

* sadd
* smembers
* srem

## zset {#zset}

* zadd
* zrange
* zrangebyscore
* zscore
* zrem
* zremrangebyscore



