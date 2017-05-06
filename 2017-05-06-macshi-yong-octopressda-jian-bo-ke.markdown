---
layout: post
title: "Mac使用Octopress搭建博客"
date: 2015-09-04 08:22:05 +0800
comments: true
categories: Mac
---

<!--more-->
一、搭建环境

* 安装`homebrew`
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```



* 使用`homebrew`升级新版本ruby替换系统自带`ruby`  
```
brew install ruby
```
* 升级`gem`版本  
```
gem update  --system 2.6.6
```
* 安装`bundler`  
```
sudo gem install bundler
```
* 升级`rake`版本
```
bundle update rake
```


二、在本地启动博客服务

* 安装博客所需要的`ruby`依赖  
```
bundler install
```  
* 安装默认主题和配置  
```
rake install
```
* 编译markdown文件，生成静态文件  
```
rake generate
```
* 本地预览  
```
rake preview
```

* 新建文章
```
rake new_post
Enter a title for your post:
```

三、将本地博客上传至`GitPage`
```
rake generate
rake deploy
```



