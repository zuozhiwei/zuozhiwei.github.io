---
layout: post
title:  thinkphp5数据库操作记录
date:   2017-1-30 20:50:00 +0800
categories: 技术
tag: thinkphp5 sql
---

* thinkphp5数据库操作：对于简单的查询和插入操作，使用助手函数很方便
* 查询是否存在
``` mysql
db('user') -> where('nick',$nick) -> where('password',$password) -> find();
```
以上语句查询结果：若不存在，则返回null，所以判断是否null即可判断是否存在以上两个条件。

* 查询具体列的值
``` mysql
db('user') -> where('nick',$nick) -> value('name');
```
以上语句查询结果：user表nick=$nick的记录中name的值。

* 查询表多个列的值
``` mysql
db('user') -> field('nick,name,address,img') -> select();
```
以上语句查询结果：查询user表nick，name，address，img列。

* 