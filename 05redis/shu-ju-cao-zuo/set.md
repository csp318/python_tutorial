# set类型 {#学习目标}

* 无序集合
* 元素为string类型
* 元素具有唯一性，不重复
* 说明：对于集合没有修改操作

## 增加 {#增加}

* 添加元素

  > sadd key member1 member2 ...

* 例1：向键'a3'的集合中添加元素'zhangsan'、'lisi'、'wangwu'

  > sadd a3 zhangsan sili wangwu

  ![](/assets/p1_43.png "增加")

## 获取 {#获取}

* 返回所有的元素

  > smembers key

* 例2：获取键'a3'的集合中所有元素

  > smembers a3

  ![](/assets/p1_44.png "获取")

## 删除 {#删除}

* 删除指定元素

  > srem key

* 例3：删除键'a3'的集合中元素'wangwu'

  > srem a3 wangwu

  ![](/assets/p1_45.png "删除")



