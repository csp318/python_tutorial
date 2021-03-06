# 分支

![](../images/github分支.png)

* 作用：
    * 区分生产环境代码以及开发环境代码
    * 研究新的功能或者攻关难题
    * 解决线上bug
* 特点：
   * 项目开发中公用分支包括master、dev
   * 分支master是默认分支，用于发布，当需要发布时将dev分支合并到master分支
   * 分支dev是用于开发的分支，开发完阶段性的代码后，需要合并到master分支

#### 模拟经理分支操作

* 对比：操作分支前的代码

    ![](../images/github经理操作分支前代码.png)

* 1.进入到经理的本地仓库`test007`

   ```
   cd Desktop/manager/test007/
   ```

* 2.查看当前分支

    ```
    git branch
    ```

    * 没有创建其他分支时，只有`master`分支

        ![](../images/github经理第一次查看master分支.png)

* 3.经理创建并切换到dev分支

   ```
   git checkout -b dev
   ```

   ![](../images/github经理创建并切换到dev分支.png)
   
* 4.设置本地分支跟踪远程指定分支（将分支推送到远程）
    
    ```
    git push -u origin dev
    ```

* 5.经理在dev分支编辑代码

   ![](../images/github经理dev编辑代码num4.png)

* 6.管理dev分支源代码：`add`、`commit`、`push`

    ![](../images/github经理dev编辑代码num4后git操作.png)

    ![](../images/github经理dev编辑代码num4后推送.png)

* 7.dev分支合并到master分支
    * 提示：只有当dev分支合并到master分支成功，张三才能获取到`num4`
    * 7.1 先切换到master分支

        ```
        git checkout master
        ```

        ![](../images/github经理合并分支切换到master分支.png)

    * 7.2 dev分支合并到master分支

        ```
        git merge dev
        ```

        ![](../images/github经理合并分支dev到master.png)

    * 7.3 经理推送合并分支操作到远程仓库
        * 合并分支默认在本地完成，合并后直接推送即可

        ```
        git push
        ```

        ![](../images/github经理合并分支dev到master推送.png)

* 8.张三同步经理合并后的`num4`
    * 只有当张三同步代码成功，分支合并才算成功

        ```
        cd Desktop/zhangsan/test007/
        git pull
        ```

        ![](../images/github张三同步分支合并后git操作.png)

        ![](../images/github张三同步分支合并后代码.png)