# 学习目标 {#学习目标}

* 能够使用StrictRedis对象对string类型数据进行增删改查

# 准备 {#准备}

* 在桌面上创建redis目录
* 使用pycharm打开 redis目录
* 创建redis\_string.py文件

```python
from redis import *
if __name__=="__main__":
    try:
        #创建StrictRedis对象，与redis服务器建立连接
        sr=StrictRedis()

    except Exception as e:
        print(e)
```

# string-增加 {#string增加}

* 方法set，添加键、值，如果添加成功则返回True，如果添加失败则返回False
* 编写代码如下

```python
from redis import *
if __name__=="__main__":
    try:
        #创建StrictRedis对象，与redis服务器建立连接
        sr=StrictRedis()
        #添加键name，值为itheima
        result=sr.set('name','itheima')
        #输出响应结果，如果添加成功则返回True，否则返回False
        print(result)
    except Exception as e:
        print(e)
```

# string-获取 {#string获取}

* 方法get，添加键对应的值，如果键存在则返回对应的值，如果键不存在则返回None
* 编写代码如下

```python
from redis import *
if __name__=="__main__":
    try:
        #创建StrictRedis对象，与redis服务器建立连接
        sr=StrictRedis()
        #获取键name的值
        result = sr.get('name')
        #输出键的值，如果键不存在则返回None
        print(result)
    except Exception as e:
        print(e)
```

# string-修改 {#string修改}

* 方法set，如果键已经存在则进⾏修改，如果键不存在则进行添加
* 编写代码如下

```python
from redis import *
if __name__=="__main__":
    try:
        #创建StrictRedis对象，与redis服务器建立连接
        sr=StrictRedis()
        #设置键name的值，如果键已经存在则进⾏修改，如果键不存在则进⾏添加
        result = sr.set('name','itcast')
        #输出响应结果，如果操作成功则返回True，否则返回False
        print(result)
    except Exception as e:
        print(e)
```

# string-删除 {#string删除}

* 方法delete，删除键及对应的值，如果删除成功则返回受影响的键数，否则则返 回0
* 编写代码如下

```python
from redis import *
if __name__=="__main__":
    try:
        #创建StrictRedis对象，与redis服务器建立连接
        sr=StrictRedis()
        #设置键name的值，如果键已经存在则进⾏修改，如果键不存在则进行添加
        result = sr.delete('name')
        #输出响应结果，如果删除成功则返回受影响的键数，否则则返回0
        print(result)
    except Exception as e:
        print(e)
```

# 获取键 {#获取键}

* 方法keys，根据正则表达式获取键
* 编写代码如下

```python
from redis import *
if __name__=="__main__":
    try:
        #创建StrictRedis对象，与redis服务器建立连接
        sr=StrictRedis()
        #获取所有的键
        result=sr.keys()
        #输出响应结果，所有的键构成⼀个列表，如果没有键则返回空列表
        print(result)
    except Exception as e:
        print(e)
```



