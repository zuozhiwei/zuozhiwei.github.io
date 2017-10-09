---
layout: post
title:  mysql数据类型之数值类型
date:   2017-3-12 8:13:00 +0800
categories: 技术
tag: mysql 数据类型
---

* 数值类型详解


| Type | Storage(Bytes) | Minimum Value(Signed/Unsigned) | Maximum Value(Signed/Unsigned)
|  --- | --- | --- | --- |
| TINYINT | 1 | -128 | 127
|        |   | 0 | 255
| SMALLINT | 2 | -32768 | 32767
|        |  | 0 | 65535
| MEDIUMINT | 3 | -8388608 | 8388607
|        |  | 0 | 16777215
| INT | 4 | -2147483648 | 2147483647
|        |  | 0 | 4294967295
| BIGINT | 8 | -9223372036854775808 | 9223372036854775807
|       |  | 0 | 18446744073709551615