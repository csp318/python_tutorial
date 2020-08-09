## Selenium(重要) 和 PhantomJS(了解)

### DHTML: 动态HTML技术
   ![](images/01_DHTML.png)
  - DHTML给爬虫带来了一些困难,举例
    * 下次发送请求需要带上上面请求中加密后的数据
    * js 进行了混淆, 让你不能看出他的逻辑, 如果硬干会消耗大量精力
    * 这个时候怎么办呢? Selenium可以控制浏览器发送请求, 获取浏览器请求到的数据,
      这个时候我们发送请求就和用户是一样的了, 正常用户能拿到数据, 我们也可以.

### Selenium 与 PhantomJS 介绍

#### Selenium

-  Selenium是一个Web的自动化测试工具,
-  Selenium 可以根据我们的指令，让浏览器自动加载页面，获取需要的数据，设置数据, 点击按钮, 甚至页面截屏，或者判断网站上某些动作是否发生
- Selenium 自己不带浏览器，不支持浏览器的功能，它需要与第三方浏览器结合在一起才能使用。

#### PhantomJS(了解)

-  是一个基于Webkit的“无界面”(headless)浏览器，经测试运行速度和有界面的Chrome差不多
-  在63版本后, Chrome也支持了无界面运行, 效率比PhantomJs高.

#### 安装

- Selenium 安装
  ```
    sudo pip install selenium
  ```
- ChromeDriver下载安装:
  - 注意下载的版本号要支持你的浏览器
  - [淘宝镜像](http://npm.taobao.org/)
  - [ChromeDriver淘宝镜像](https://npm.taobao.org/mirrors/chromedriver)
  - 注意查看[chromedriver支持的版本](https://npm.taobao.org/mirrors/chromedriver/2.38/notes.txt)
  - Linux 或 Mac 解压后直接拷贝到usr/local/bin 或 usr/bin 下即可; 也可以制作软连接放到上面的两个路径下
  - 在Linux或Mac中如果报关于Permission的错误, 是因为chromedriver这个文件没有执行权限, 就修改chromedriver文件的权限为 777
    - chmod 777 chromedriver


