### Selenium入门
- 加载网页：
  - from selenium import webdriver
  - driver = webdriver.Chrome() `如果是Windows()中传入driver的路径: “c:…/pantomjs.exe”`
  - driver.get("http://www.baidu.com/")
  - driver.save_screenshot("baidu.png")
- 定位和操作：
  - driver.find_element_by_id(“kw”).send_keys(“python”)
  - driver.find_element_by_id("su").click()
- 查看请求信息：
  - driver.page_source
  - driver.get_cookies()
  - driver.current_url
- 退出
  - driver.close() #退出当前页面
  - driver.quit()  #退出浏览器

- 案例打开百度搜索传智播客

```python
from selenium import webdriver
from selenium.webdriver.chrome.options import Options
import time

# 创建Options对象
options = Options()
options.set_headless()

# 创建Chrome的驱动对象
driver = webdriver.Chrome(options=options)

# 加载页面 百度首页
driver.get("http://www.baidu.com")
# 保存当前界面
driver.save_screenshot("baidu.png")

# 搜索传智播客
driver.find_element_by_id("kw").send_keys("传智播客")
# 点击搜索按钮
driver.find_element_by_id("su").click()

# 获取页面内容
# print(driver.page_source) #这个内容就和Elements中内容一样
# 获取当前的URL
print(driver.current_url)
# 获取cookie信息
cookies = driver.get_cookies()
# print(cookies)
# 处理成为我们发送请求时候,可以使用cookie
cookies = {cookie["name"]:cookie["value"]  for cookie in cookies}
print(cookies)

time.sleep(3)

# 关闭当前窗口
# driver.close()
# 退出浏览器
driver.quit()
```

- 总结(我们所得到的)
- 如何在代码中使用selenium
  - 导入模块: 
    - from selenium import webdriver
  - 创建Chrome的webdriver对象
    - driver = webdriver.Chrome() `如果是Windows()中传入driver的路径: “c:…/pantomjs.exe”`
  - 发送请求
    - driver.get("http://www.baidu.com/")
  - 根据id定位元素并进行操作
    - driver.find_element_by_id(“kw”).send_keys(“python”)  # 找到id为kw的输入框, 填写: python
    - driver.find_element_by_id("su").click() # 找到id为su的, 进行单击
  - 查看请求信息：
    - driver.page_source # 获取页面的源码
    - driver.get_cookies() # 获取cookie信息
    - driver.current_url   # 获取当前的URL 
  - 退出
    - driver.close() #关闭当前窗口(选项卡)
    - driver.quit()  #退出浏览器


### 操作cookie的方法(扩展阅读)

```python
  {cookie[‘name’]: cookie[‘value’] for cookie in driver.get_cookies()}
  driver.delete_cookie("CookieName")
  driver.delete_all_cookies()
```