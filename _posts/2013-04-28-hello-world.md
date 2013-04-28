---
layout: post
title: "搭建github+jekyll静态博客所踩过的坑"
description: ""
category: diary
tags: [jekyll, github]
---
{% include JB/setup %}



终于把本地的jekyll搭建成功了，其实很简单的一个过程，让我弄了一下午加一晚上，这里记录下踩过的坑。

- jekyll的安装。jekyll是一个ruby写的静态博客转换的程序，windows下配置ruby的环境，需要先安装ruby和devkit，网上其实有很多教程。就是先安装ruby，再在命令行中安装devkit。devkit是一个模拟unix环境的工具，受传统思想影响，我一直在cygwin的命令行中操作，结果无数次失败，出现莫名其妙的原因。后来才想到，那些教程里并没说是在cygwin中，应该就是在dos命令行中。

- 第二个问题是版本问题。一向以为最新版本就是最好的，结果用ruby2.0安装好jekyll后，发现启动时一直失败，后网上看到别人说是2.0的原因，选用ruby1.9.3就OK了。版本问题，再次上这个当，以后一定要注意。特别是自己不熟悉的东西，配置时一定要选用对的版本。

- jekyll终于安装成功也可以运行了，可以运行后打开localhost:4000出现403错误，本来以为权限问题，其它是我的jekyll网站代码有问题，导致解析失败，所以_site/下并没有生成静态页面。
