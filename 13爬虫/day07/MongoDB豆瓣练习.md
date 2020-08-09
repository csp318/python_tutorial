### mongodb 豆瓣练习
- 尝试将douban.tv1中的数据恢复到自己的电脑中，具体如何操作？
  
  ```js
    mongorestore -d douban --dir douban
  ```

- 完成上述操作后完成以下问题：
  1. 获取每条数据中的title，count(所有评分人数),rate(评分),country(国家)的这些字段
  
  ```js
    db.tv1.aggregate(
      {$project:{_id:0,title:1, count:'$rating.count', rate:'$rating.value', country:'$tv_category'}}
    )

  ```
  
  2. 获取上述结果中的不同国家电视剧的数据量
  
  ```js
    db.tv1.aggregate(
      {$project:{_id:0,title:1, count:'$rating.count', rate:'$rating.value', country:'$tv_category'}},
      {$group:{_id:'$country', tv_count:{$sum:1}}},
      {$project:{_id:0,country:'$_id', tv_count:1}}
    )
  ```
  
  3. 获取上述结果中分数大于8分的不同国家电视剧的数据量

  ```js
    db.tv1.aggregate(
      {$match:{"rating.value":{$gt:8}}},
      {$project:{_id:0,title:1, count:'$rating.count', rate:'$rating.value', country:'$tv_category'}},
      {$group:{_id:'$country', tv_count:{$sum:1}}},
      {$project:{_id:0,country:'$_id', tv_count:1}}
    )
  ```