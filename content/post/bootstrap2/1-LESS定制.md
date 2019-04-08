---
title: "Bootstrap2-1.LESS定制"
author: "Heaven Jiang"
date: 2016-09-17T19:30:10+08:00
draft: false
tags: ["bootstrap2"]
categories: ["bootstrap2"]
---

# Bootstrap2-1.LESS定制

## Less 简介
>CSS（层叠样式表）是一门历史悠久的标记性语言，同 HTML 一道，被广泛应用于万维网（World Wide Web）中。HTML 主要负责文档结构的定义，CSS 负责文档表现形式或样式的定义。作为一门标记性语言，CSS 的语法相对简单，对使用者的要求较低，但同时也带来一些问题：CSS 需要书写大量看似没有逻辑的代码，不方便维护及扩展，不利于复用，尤其对于非前端开发工程师来讲，往往会因为缺少 CSS 编写经验而很难写出组织良好且易于维护的 CSS 代码，造成这些困难的很大原因源于 CSS 是一门非程序式语言，没有变量、函数、SCOPE（作用域）等概念。LESS 为 Web 开发者带来了福音，它在 CSS 的语法基础之上，引入了变量，Mixin（混入），运算以及函数等功能，大大简化了 CSS 的编写，并且降低了 CSS 的维护成本，就像它的名称所说的那样，LESS 可以让我们用更少的代码做更多的事情。


## LESS 原理及使用方式
>本质上，LESS 包含一套自定义的语法及一个解析器，用户根据这些语法定义自己的样式规则，这些规则最终会通过解析器，编译生成对应的 CSS 文件。LESS 并没有裁剪 CSS 原有的特性，更不是用来取代 CSS 的，而是在现有 CSS 语法的基础上，为 CSS 加入程序式语言的特性。**LESS 是动态的样式表语言，通过简洁明了的语法定义，使编写 CSS 的工作变得非常简单。本文将通过实例，为大家介绍这一框架。**

## 代码清单

### 1. LESS文件
>LESS代码
``` css
@color: #4D926F;
#header{
    color: @color;
}
h2{
    color: @color;
}
``` 

### 2. CSS文件
>编译生成的CSS文件如下
``` css
@color: #4D926F;
#header{
    color: @color;
}
h2{
    color: @color;
}
``` 

## LESS文件怎么引入项目
### 一、使用 JavaScript（开发阶段）
>只需要简单的引用 less.js 文件并重新加载页面。js 文件就会编译 less。

``` javascript
<link rel="stylesheet/less" href="/path/to/bootstrap.less">
<script src="/path/to/less.js"></script>
```

### 二、编译（发布阶段）
>方法①安装Node.js环境（附带npm），在Bootstrap的根目录下运行 make 即可编译CSS方法

>方法②koala_2.0.4_portable
