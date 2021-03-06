# 多人协同开发

* 1.代码编辑界面介绍：此处使用`gedit`做演示
    * 代码编辑界面左边为模拟经理的操作
    * 代码编辑界面右边为模拟张三的操作

    ![](../images/github代码编辑界面介绍.png)

* 2.模拟张三先编辑`login.py`文件代码
    * 进入张三本地仓库：`cd Desktop/zhangsan/test007`
    * 编辑代码：`num1 = 10`
    * 本地仓库记录版本：`git commit -am '第一个变量'`
    * 推送到远程仓库：`git push`

        ![](../images/github张三编辑num1.png)

        ![](../images/github张三编辑num1git操作.png)

        ![](../images/github张三编辑num1推送后.png)

* 3.模拟经理后编辑`login.py`文件代码
    * 进入经理本地仓库：`cd Desktop/manager/test007/`
    * 经理同步服务器代码：`git pull`
    * 编辑代码：`num2 = 20`
    * 本地仓库记录版本：`git commit -am '第二个变量'`
    * 推送到远程仓库：`git push`

        ![](../images/github经理同步num1.png)

        ![](../images/github经理编辑num2.png)

        ![](../images/github经理编辑num2git操作.png).

        ![](../images/github经理编辑num2推送后.png)

* 4.模拟张三同步服务器代码
    * 本次可以把`num2`同步到张三的本地仓库

        ![](../images/github张三同步num2.png)

* 5.按照以上`2-3-4`步骤循环操作，即可实现基本的协同开发

* 6.总结：
    * 要使用git命令操作仓库，需要进入到仓库内部
    * 要同步服务器代码就执行：`git pull`
    * 本地仓库记录版本就执行：`git commit -am '版本描述'`
    * 推送代码到服务器就执行：`git push`
    * 编辑代码前要先`pull`，编辑完再`commit`，最后推送是`push`

