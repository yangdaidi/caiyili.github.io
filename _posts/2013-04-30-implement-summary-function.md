---
layout: post
title: "实现博文预览功能"
description: ""
category: note
tags: [jekyll]
---
{% include JB/setup %}

今天参照[午夜咖啡][1]实现了预览的功能。  
主要思想是在发布的博文中加入一个`<!--more-->`的标签，它不会影响输出。然后在`post.content`用`<!--more-->`来`split`
其实实现思想还是蛮简单的，我怎么开始就没想到呢？

[1]: http://jolestar.com/