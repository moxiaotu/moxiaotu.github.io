---
layout: post 														# 指定使用的模板文件，“_layout” 目录下的模板文件名决定变量名
title: 'windows系统安装Jekyll'										# 文章的标题
date: 2017-10-04													# 覆盖文章名中的日期
author: 教程														# 文章的类别
cover: 'http://on2171g4d.bkt.clouddn.com/jekyll-banner.png'
tags: jekyll														#博客标签
---

> 写给一样的小白交流学习，大神请无视，有错误请联系指出.

# 下载Ruby
下载地址
[https://rubyinstaller.org/downloads](https://rubyinstaller.org/downloads)<br/>
ruby2.3.3(x64)下载<br/>
[https://dl.bintray.com/oneclick/rubyinstaller/rubyinstaller-2.3.3-x64.exe](https://dl.bintray.com/oneclick/rubyinstaller/rubyinstaller-2.3.3-x64.exe)
![图片](/assets/img/Jekyll安装001.jpg)

## ruby安装
![图片](/assets/img/Jekyll安装002.jpg)
![图片](/assets/img/Jekyll安装003.jpg)
### 重点勾选添加到系统环境变量！！！
![图片](/assets/img/Jekyll安装004.jpg)
![图片](/assets/img/Jekyll安装005.jpg)
### 之前没勾选添加到系统环境变量的现在手动添加<br/>
安装路径<br/>
```RUBY_HOME```
当前安装的ruby目录为主 <br/>
![图片](/assets/img/Jekyll安装006.jpg)
```Path```<br/>
```%RUBY_HOME%\bin```<br/>
在path里面后面添加 %RUBY_HOME%\bin;
![图片](/assets/img/Jekyll安装007.jpg)
### 查看是否安装成功
打开```cdm```命令行面板，输入```gem -v```，如果显示出了版本号，则说明安装成功。
![图片](/assets/img/Jekyll安装008.jpg)
![图片](/assets/img/Jekyll安装009.jpg)

## devkit安装






