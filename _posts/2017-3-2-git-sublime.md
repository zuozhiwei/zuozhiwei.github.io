---
layout: post
title:  sublime配置git
date:   2017-3-2 17:59:00 +0800
categories: 技术 git sublime
tag: git sublime
---

### 1.下载并安装git

下载链接：(免安装)
[https://github.com/git-for-windows/git/releases/download/v2.12.0.windows.1/PortableGit-2.12.0-64-bit.7z.exe](https://github.com/git-for-windows/git/releases/download/v2.12.0.windows.1/PortableGit-2.12.0-64-bit.7z.exe)

下载之后双击文件，并提示解压目录，选择合适目录后确定，我选择的是
> E:\tools\git\

### 2.配置环境变量

右键我的电脑-->选择属性-->选择高级系统设置-->选择环境变量-->双击path-->添加git的cmd路径(例如：E:\tools\git\cmd)

### 3.生成秘钥

* 首先设置本地姓名与邮箱
``` git
git config --global user.name "zuozhiwei"
git config --global user.email "zuozhiwei0@gmail.com"
```
* 然后生成秘钥公钥
``` git
ssh-keygen -t rsa -C "zuozhiwei0@gmail.com"
```
### 4.在网站上输入公钥

* 我使用的coding网站， github同理，coding比github访问速度更快
* 打开网站，找到公钥管理输入名称
* 打开c盘下的用户目录下的用户名目录的.ssh目录中的id_rsa.pub,我的路径如下：
> C:\Users\zuozhiwei\.ssh\id_rsa.pub
* 使用记事本或者sublime打开此文件，复制内容到网站上
* 保存即可

### 5.配置sublime的git插件

* sublime安装git插件
* 编辑git配置文件
> E:\tools\Sublime Text 3\Data\Packages\User\Git.sublime-settings
写入：
``` html
{
  "git_command": "E:/tools/git/cmd/git.exe"
}
```