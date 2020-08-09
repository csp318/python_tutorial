# 学习目标 {#学习目标}

* 能够写出删除指定键的相关命令

# 键命令 {#键命令}

* 查找键，参数支持正则表达式

  > keys pattern

* 例1：查看所有键

  > keys \*

  ![](/assets/p1_20.png "查看所有键")

* 例2：查看名称中包含a的键

  > keys 'a\*'

  ![](/assets/p1_21.png "查看键")

* 判断键是否存在，如果存在返回1，不存在返回0

  > exists key1

* 例3：判断键a1是否存在

  > exists a1

  ![](/assets/p1_22.png "判断键是否存在")

* 查看键对应的value的类型

  > type key

* 例4：查看键a1的值类型，为redis支持5中类型的一种

  > type a1

  ![](/assets/p1_23.png "查看值类型")

* 删除键及对应的值

  > del key1 key2 ...

* 例5：删除键a2、a3

  > del a2 a3

  ![](/assets/p1_24.png "删除键")

* 设置过期时间，以秒为单位

* 如果没有指定过期时间则一直存在，直到使用DEL移除

  > expire key seconds

* 例6：设置键'a1'的过期时间为3秒

  > expire 'a1' 3

  ![](/assets/p1_25.png "设置过期时间")

* 查看有效时间，以秒为单位

  > ttl key

* 例7：查看键'bb'的有效时间

  > ttl bb

  ![](/assets/p1_27.png "查看有效时间")



