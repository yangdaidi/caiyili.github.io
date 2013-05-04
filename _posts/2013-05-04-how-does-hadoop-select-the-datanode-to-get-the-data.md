---
layout: post
title: "Hadoop根据什么来选择从哪个数据结点提取数据"
description: ""
category: note
tags: ['hadoop','MapReduce']
---
{% include JB/setup %}

今天在为我的项目画UML图时，无意中发现了一个困扰了我很久的问题——Hadoop怎样选择从哪个节点获取数据  
在我的hadoop和lucene整合项目中，采用的方法是利用MapReduce编程模型来控制并发的lucene查询，在每个datanode上
都部署一个完整的lucene索引，然后根据配置文件，让每个datanode上的TaskTracker读取本地的lucene索引，结果以
`<score,resultmap>`的方式传给`map`，再让MapReduce做聚合过程。  
可是怎样保证`map`任务只读取本地的lucene索引呢？一直以为`map`从哪个节点取数据是不可以控的，今天无意中发现原来
`InputSplit`提供的一个接口`getLocations() `就是决定切分的数据来自哪些数据结点列表的。  
<!-- more -->