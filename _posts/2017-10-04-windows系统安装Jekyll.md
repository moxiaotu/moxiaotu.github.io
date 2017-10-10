---
layout: post 														# 指定使用的模板文件，“_layout” 目录下的模板文件名决定变量名
title: 'windows系统安装Jekyll'										# 文章的标题
date: 2017-10-04													# 覆盖文章名中的日期
author: 教程														# 文章的类别
cover: 'http://on2171g4d.bkt.clouddn.com/jekyll-banner.png'
tags: jekyll														#博客标签
---

> 写给一样的小白交流学习，大神请无视，有错误请联系指出.

# Ruby
## 下载Ruby
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
在```path```里面后面添加 ```%RUBY_HOME%\bin;```
![图片](/assets/img/Jekyll安装007.jpg)
### 查看是否安装成功
打开```cdm```命令行面板，输入```gem -v```，如果显示出了版本号，则说明安装成功。
![图片](/assets/img/Jekyll安装008.jpg)
![图片](/assets/img/Jekyll安装009.jpg)

# devkit
## 下载devk
如果使用rubyinstaller安装包需单独下载devkit<br/>
DevKit(x64)下载<br/>
[http://cdn.rubyinstaller.org/archives/devkits/DevKit-mingw64-64-4.7.2-20130224-1432-sfx.exe](http://cdn.rubyinstaller.org/archives/devkits/DevKit-mingw64-64-4.7.2-20130224-1432-sfx.exe)
这东东是个压缩包，直接解压到指定的文件夹就好了，不然会目录冒出14个文件。
![图片](/assets/img/Jekyll安装010.jpg)

## ruby安装
###创建 ```config.yml``` 文件
打开命令行，进入devkit的解压目录<br/>
```ruby dk.rb init``` 初始化创建```config.yml```文件
![图片](/assets/img/Jekyll安装011.jpg)
### 查看```config.yml```
打开所创建的```config.yml```文件，查看最后是否自动加上```- D:/ToolKits/Ruby/Ruby21-x64```，如果没有手动加上就可以了，这里的目录为你的Ruby的安装目录，保存文件并退出。
![图片](/assets/img/Jekyll安装012.jpg)
然后回到命令行窗口内进行安装。<br/>
```ruby dk.rb install```
![图片](/assets/img/Jekyll安装013.jpg)
### 更改默认的source源
这里推荐一个来自简书的博主：撒网要见鱼的方法。
鉴于官方源无法访问，所以我们得更换为可以使用的源，这里推荐使用```ruby china```源，大致步骤如下<br/>
•	先键入命令```gem sources -l``` 查看当前已经添加的源(默认应该是同时有官方源和淘宝源) <br/>
•	然后通过 ```gem sources -r https://rubygems.org/``` ```gem sources -r https://ruby.taobao.org/``` 分别移除官方源和淘宝源 (注意，请对比实际，移除自己已经添加的源即可，可以改为自己上一步中查询出来的地址) <br/>
•	通过 ```gem sources -a http://gems.ruby-china.org``` 添加了ruby china的可用源<br/>
•	修改来源后可以通过```gem sources -l```查看是否正确修改<br/>
![图片](/assets/img/Jekyll安装014.jpg)

# Jekyll
## 安装 Jekyll
### 查看gem
首先要确保 gem 是否已经正确安装
![图片](/assets/img/Jekyll安装015.jpg)
### 安装依赖包bundler
安装jekyll前先安装依赖包bundler，下述命令即可安装<br/>
```gem install bundler```
![图片](/assets/img/Jekyll安装016.jpg)
### 命令行执行安装 Jekyll
```gem install Jekyll```
![图片](/assets/img/Jekyll安装017.jpg)
### 查看jekyll
检测jekyll是否安装成功<br/>
```jekyll -v```
![图片](/assets/img/Jekyll安装018.jpg)
### 创建Jekyll模板
命令行或者Git Bash下运行 ```jekyll new moxiaotu.github.io```就可以创建出一个最基本的Jekyll模板
![图片](/assets/img/Jekyll安装019.jpg)
### 目录结构
其目录结构如图<br/>
Jekyll经过了多次版本迭代，对于默认创建的目录也有较大的变化：<br/>
•	posts:用于存放博客的文件夹，一般采用markdown语法写成 <br/>
•	coinfig.ym：jekyll的配置文件，里面可以定义很多配置参数，具体可查看 官网<br/>
•	about.md:可以看作 content 填充模板，build后生成html文件，相当于一个页面<br/>
•	index.md:同上
![图片](/assets/img/Jekyll安装020.jpg)
### 启动Jekyll本地服务
![图片](/assets/img/Jekyll安装021.jpg)
### 启动Jekyll服务常见问题解决
启动服务缺少模块时会出现下面的情(模块名称可能不相同)<br/>
解决方法:缺少哪个模块就安装相应模块<br/>
```gem install 模块名称```
![图片](/assets/img/Jekyll安装022.jpg)

#### END




