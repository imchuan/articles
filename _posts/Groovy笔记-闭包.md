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

参数化的闭包

	// 参数化
    def cols1 = { str -> println str }
    cols1.call("Leon")
    cols1("Hello World")

单个隐藏参数

    // 单个隐参数
    def cols2 = {println it}
    cols2("Hello cols2")

访问变量，闭包只能访问已经定义过的变量

    // 访问变量
    def wel = "Hello"
    def say = { params -> println "${wel},${params}" }
    say("Leon")

    wel = "Welcome"		// wel变量值改变
    say("Leon")
# 闭包在集合中的应用

遍历集合

    [1,2,3,4,5].each { println it}  // 输出列表中每个元素
    def student = ["name":"Leon", "age": 25]
    student.each { println "${it.key} = ${it.value}"}

条件元素

    def nums = [1, 2, 3, 4, 5]
    nums.each { num -> if (num == 2) println num }

    def result = nums.find({ it > 3 }) // 返回第一个符合条件的值
    println "result = $result"



























