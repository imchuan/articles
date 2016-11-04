---
title: Groovy笔记-闭包
date: 2016-11-4 11:29:20
categories: Groovy
tags: Groovy笔记
---
Groovy闭包是一种表示可执行代码块的方法，闭包也是对象，可以像方法一样传递参数，也可以在需要时执行。像方法一样，在定义的过程中，闭包也可以使用一个或者多个参数，闭包的一个重要特性就是，它们可以访问属性信息，这就意味着在声明闭包之后，闭包可以使用并修改其作用域内的所有变量值。
闭包最常见的用途是处理集合
<!-- more -->

# 闭包
语法`{comma-separated-formal-parameter-list -> statement-list}`
定义一个闭包

    def clos = {println "Hello world"}
    clos.call() 	// 调用




























