# 克隆项目

* 准备经理的文件 `Desktop/manager/`
* 准备张三的文件 `Desktop/zhangsan/`

#### 经理的工作

* 立项：克隆远程仓库+配置身份信息+创建项目+推送项目到远程仓库

* 1.克隆远程仓库的命令

    ```
    cd Desktop/manager/
    git clone https://github.com/zhangxiaochuZXC/test007.git
    ```

* 2.克隆远程仓库到本地

    ![](../images/github经理克隆远程仓库02.png)
    

* 3.克隆成功后查看经理的文件

    ![](../images/github经理克隆远程仓库成功后.png)

* 4.配置经理身份信息

    ```
    cd Desktop/manager/test007/
    git config user.name '经理'
    git config user.email 'manager@163.com'
    ```

    ![](../images/github经理配置个人信息后.png)

* 5.创建项目

    ![](../images/github经理创建项目.png)

* 6.推送项目到远程仓库

    ```
    # 工作区添加到暂存区
    git add .
    # 暂存区提交到仓库区
    git commit -m '立项'
    # 推送到远程仓库
    git push
    ```

    ![](../images/github经理推送项目到远程仓库.png)

    ![](../images/github经理推送项目到远程仓库后.png)
    
* 在 push 的时候需要设置账号与密码，该密码则是 github 的账号与密码
    - 如果在每次 push 都需要设置账号与密码，那么可以设置记住密码
    ```
    设置记住密码（默认15分钟）：
    git config --global credential.helper cache
    如果想自己设置时间，可以这样做(1小时后失效)：
    git config credential.helper 'cache --timeout=3600'
    长期存储密码：
    git config --global credential.helper store
    ```
> 在以后的项目开发过程中，Pycharm 可以自动记住密码

#### 张三的工作

* 获取项目：克隆项目到本地、配置身份信息

* 1.克隆项目到本地

    ```
    cd Desktop/zhangsan/
    git clone https://github.com/zhangxiaochuZXC/test007.git
    ```

    ![](../images/github张三克隆远程仓库02.png)

* 2.克隆成功后查看张三的文件

    ![](../images/github张三克隆远程仓库后.png)

* 3.配置张三身份信息

    ```
    cd Desktop/zhangsan/test007/
    git config user.name '张三'
    git config user.email 'zhangsan@163.com'
    ```

> 张三身份信息配置成功后即可跟经理协同开发同一个项目

