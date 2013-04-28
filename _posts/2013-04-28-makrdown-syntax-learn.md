---
layout: post
title: "makrdown语法学习笔记"
description: "markdown 学习过程中的一些笔记"
category: note
tags: [markdown]
---
{% include JB/setup %}
<link rel="stylesheet" href="http://yandex.st/highlightjs/7.3/styles/default.min.css">
<script src="http://yandex.st/highlightjs/7.3/highlight.min.js"></script>

# 总体内容 #
* 标题
* 无序列表
* __强调__
* 有序列表
* 代码块
* 区间引用 
* 超链接/图片
* 相关资源


## 有序列表 ##

1. 有序列表可以用一个数字加一个点号
2. 数字可以不按顺序
2. 像这条，前面写的是2，但markdown分自动转换成3
4. 无序列表前面可以用* 或+ 或- 
	* 列表还可以嵌套
	* 这两个就是嵌套的列表
 
## 代码块 ##
	//代码前面加四个空格会自动成代码块
	#include <stdio.h> 
	int main () {
		printf(" hello world \n") ;
	} 

## 区间引用Blockquotes ##
>引用区间就是有前面加一个>号  
区间里同一个段落前面的还可以懒惰地省掉  
> ### 区间引用还可以有标题【这是一个标题】。
> 
> 1.   同样可以有列表。
> 1.   这是第二行列表项。
>   
> 
>         //也可以有代码块，前面与>有一个空格外，还需要加2*4个空格或2个tab
>         return shell_exec("echo $input | $markdown_script");

## 超链接/图片链接 ##
* 链接有两种方式
	1. 直接一个方括号后接一个圆括号。
如 [markdown语法学习网站](http://wowubuntu.com/markdown/ "wowubuntu")  _这里面的链接怎么打不开呢？_
	2. 两个方括号，第一个是链接名称，第二个是地址引用，地址可以在后面任意一个地方标注。  
	如：[markdown在线编辑器][markdown online edit]

* 图片链接的方式与超链接相似，只是在前面加一个！
	1. 不过workflowy里好像不能显示图片 ![武汉大学](http://www.whu.edu.cn/img/main.jpg)


## 相关资源 ##
* 请[Google](https://www.google.com) "**markdown 语法**" "**markdown 在线编辑器**"
* 推荐网站
	- [markdown语法学习网站] <http://wowubuntu.com/markdown/>
	- markdown在线编辑器<http://mahua.jser.me/>
	- 让workflowy支持markdown语法的Chrome插件 .<https://chrome.google.com/webstore/detail/workflowy-for-coders/hogpngcijkfmbfijfkaapeejhijipddp>



[markdown online edit]: http://mahua.jser.me/ "mahua"  