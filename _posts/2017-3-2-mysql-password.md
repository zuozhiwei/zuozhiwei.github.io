---
layout: post
title:  mysql修改密码
date:   2017-3-2 10:15:00 +0800
categories: 技术 mysql
tag: mysql password
---

* 首次安装mysql，密码默认为空，首次修改密码代码如下

``` mysql
set password for root@localhost = password('zuozuo');
```
