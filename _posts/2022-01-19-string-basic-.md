---
layout: post
title:  "字符串基础"
date:   2022-01-19 22:30:00
categories: 基础知识
tags: [string]
---

# String

- String 被声明为 final，因此它不可被继承
- Java 8 中，String 内部使用 char 数组存储数据。
- Java 9 之后，String 类的实现改用 byte 数组存储字符串，同时使用 coder 来标识使用了哪种编码。
- 对String对象的任何改变都不影响到原对象，相关的任何change操作都会生成新的对象
  - String Pool 的需要。如果一个 String 对象已经被创建过了，那么就会从 String Pool 中取得引用。只有 String 是不可变的，才可能使用 String Pool。
  - 安全性。String 经常作为参数，String 不可变性可以保证参数不可变。如网络传输，因此字符串是线程安全


> 问题：new String("abc") 创建了多少个对象？
