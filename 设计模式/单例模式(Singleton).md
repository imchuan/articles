---
title: 单例模式(Singleton)
date: 2016-11-9 10:40:50
categories: 设计模式
tags: 设计模式
---
确保一个类只有一个实例,并提供一个全局的访问点
<!-- more -->
# 经典实现

    public class Singleton {
        private static Singleton instance;

        private Singleton() {
        }

        public static Singleton getInstance() {
            if (instance == null) {
                return new Singleton();
            }
            return instance;
        }
    }

# 多线程
1. 通过**synchronized**关键字，修饰getInstance方法，确保线程安全

        public synchronized static Singleton getInstance() {
            if (instance == null) {
                return new Singleton();
            }
            return instance;
        }
2. 在类加载时就创建类的静态变量

        private static Singleton instance = new Singleton();

        private Singleton() {
        }

        public synchronized static Singleton getInstance() {
            return instance;
        }

3. 用双重检查加锁

        private static Singleton4instance;

        private Singleton() {
        }

        public static Singleton getInstance() {
            if (instance == null) {
                synchronized (Singleton.class) {
                    if (instance == null) {
                        return new Singleton();
                    }
                }
            }
            return instance;
        }

可根据业务场景，灵活的使用单例模式，来达到最优的效果