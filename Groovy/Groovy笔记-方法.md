---
title: Groovy笔记-方法
date: 2016-11-4 11:09:20
categories: Groovy
tags: Groovy笔记
---
# 方法
通过关键字def声明一个方法，如果一个方法不带参数，需要使用**()**，并且括号不能省略

    def getName(){
		println "Hello"
    }
    getName() // 方法调用

使用变量

    def add() {
        def a = 1
        def b = 2
        println a + b
    }

    add()

带参数的方法

    def add(a, b) {
        println a + b
    }

    add(1, 2)

参数默认值，方法中的形参可以指定默认参数，默认参数只能出现在形参列表的最后面

    def getName(name = "Leon") {
        println name
    }

    getName()
    getName("Leon Liu")

    // 输出
    Leon
    Leon Liu

方法返回值，使用**return**关键字，return关键字是可选的，如果省略，则代码的最后一条语句的值就是方法的返回值

    def subtract(a, b) {
        return a - b
    }

    println subtract(2, 1)

    def subtract2(a, b) {
        a - b		// 省略return
    }

    println subtract(2, 1)

# 作用域
定义内的变量称作局部变量，局部变量只能在方法体中有效




























