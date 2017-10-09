---
layout: post
title:  wamp的phpmyadmin无法登陆
date:   2017-1-29 9:36:00 +0800
categories: 技术
tag: wamp phpmyadmin password
---

### mysql控制台修改密码，导致phpmyadmin无法登陆

* 因为密码已改，而PHPmyadmin的登陆配置文件中密码为初始的空值，先修改配置文件
* 配置文件路径在：```\wamp\apps\phpmyadmin4.1.14```目录下有```config.inc.php```文件。
* 编辑上述文件中的```$cfg['Servers'][$i]['password']= ''```,设置当前密码