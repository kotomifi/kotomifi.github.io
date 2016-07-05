---
layout: post
title: golang 控制台输入输出
date: 2016-05-21
categories: blog
tags: [golang,io, console]
description: golang文件操作总结。

---
# golang 控制台输入输出
## 控制台输入
获取键盘输入最简单的方法是使用fmt包提供的Sacn和Sscan家族的函数。具体如下：

**Sscan使用**

	fmt.Prnitln("Please input your name: ")
	// 并不是读取一行到一个变量里，而是读取console的一行，把按空格划分的值存入设置的变量中
	fmt.Scanln(&firstName, &lastName)
	
	// 每个变量之间用空格分隔
	fmt.Scanf("%s %s", &firstName, &lastName)
	
**Sscanf使用**

	var s string
	var f float32
	var i int
	
	var input = "56.12 / 5212 / Go"
	var format = "%f / %d / %s"
	fmt.Sscanf(input, format, &f, &i, &s)
	fmt.Println(f, i, s)
	
	// 打印结果如下：
	56.12 5212 Go