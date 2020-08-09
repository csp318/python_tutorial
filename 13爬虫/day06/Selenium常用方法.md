## selenium定位页面元素
  - 用法：
    - find_element_by_id (返回一个,如果没有就报错了)
    - find_elements_by_xpath （返回一个列表,如果没有就返回一个空列表）
    - find_elements_by_link_text (根据文本内容返回元素列表, 如果没有返回空列表)
    - find_elements_by_partial_link_text (根据文件部分内容返回元素列表, 如果没有返回空列表)
    - find_elements_by_tag_name(根据标签名[节点名]返回元素元素列表, 如果没有返回空列表)
    - find_elements_by_class_name(根据class属性对应值范围元素列表, 如果没有返回空列表)
    - find_elements_by_css_selector(根据css选择器返回元素列表, 如果没有返回空列表)
  - 注意点:
    - find_element 和find_elements的区别：
      - find_element: 返回找到第一个元素,如果没有报错
      - find_elements: 返回找到的所有元素列表, 如果没有找到返回空列表

    - by_link_text和by_partial_link_text的区别：
      - by_link_text: 全部文本都一样
      - by_partial_link_text: 包含某个文本
    - by_xpath只能获取元素, 要获取属性和文本需要使用get_attribute(属性名) 和.text

## 获取元素的数据与操作

* get_attribute(key) : 获取节点上的属性
* text属性: 获取该节点上以及子节点的文本
* click(): 点击控件

#### 测试代码

- 代码

```python
from selenium import webdriver
import time

dr = webdriver.Chrome()

dr.get('http://www.baidu.com')

el = dr.find_element_by_id('kw')
el = dr.find_element_by_name('wd')
el = dr.find_element_by_xpath('//*[@id="kw"]')

# 通过链接文本进行定位
el = dr.find_element_by_link_text('hao123')
el = dr.find_element_by_partial_link_text('hao12')
# el.click()

# 通过class值定位元素
el = dr.find_element_by_class_name('head_wrapper')
print(el.get_attribute('class'))

# 通过css选择器定位元素
el = dr.find_element_by_css_selector('#kw')
print(el)

# send_keys是往可以输入内容的标签中输入数据
el.send_keys('python23')
time.sleep(3)
el.clear()
el.send_keys('python爬虫')


el_submit = dr.find_element_by_id('su')
# 模拟点击
el_submit.click()

time.sleep(3)
dr.quit()
```

- 总结(我们GET到的)
   - 使用driver获取的元素,直接使用xpath只能获取元素,不能取出元素上的数据
   - 如果要取出属性,需要使用get_attribute的方法获取
   - 如果要取内容,需要使用text属性