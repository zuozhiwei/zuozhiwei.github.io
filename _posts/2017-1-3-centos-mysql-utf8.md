---
layout: post
title:  mysql操作记录
date:   2017-1-7 10:50:00 +0800
categories: 技术
tag: mysql centos
---

* 设置id自增

首先id需要int类型，然后id是主键，才可设置自增，语句如下
``` mysql
create table teacher(
    id int(10) auto_increment primary key,
    name varchar(20)
    )
```

* 导入sql文件

在我的项目中，导入sql文件代码如下：
``` mysql
    source /var/www/html/467/lawedu/teacher.sql
```

* 设置utf8编码

首先查询:
``` mysql
    show variables like '%character%';
    show variables like '%collation%';
```
然后设置各项编码
``` mysql
    set character_set_client = utf8;
    set character_set_server = utf8;
    set character_set_connection = utf8;
    set character_set_database = utf8;
    set character_set_results = utf8;
    set collation_connection = utf8_general_ci;
    set collation_database = utf8_general_ci;
    set collation_server = utf8_general_ci;
```