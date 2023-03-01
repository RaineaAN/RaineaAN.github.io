---
title: Markdown 链接 (6)
date: 2021-09-22 09:57:45
categories: [学习笔记,Markdown]
tags: [Markdown学习笔记,Markdown]
top_img: https://cdn.staticaly.com/gh/hennessey-v/pic@master/bg/blue-lake-v1.jpg
---

# Markdown 链接

链接使用方法如下：

```
[链接名称](链接地址)

或者

<链接地址>
```

例如：

```
这是一个链接 [菜鸟教程](https://www.runoob.com)
```

显示结果如下：

![](https://hennessey02.coding.net/p/Pic/d/Pic01/git/raw/master/img//49E6CB42-F780-4DA6-8290-DC757B51FB9A.jpg)

直接使用链接地址：

```
<https://www.runoob.com>
```

显示结果如下：

![](https://www.runoob.com/wp-content/uploads/2019/03/9BFF60A1-DD71-4B63-987B-4665B31C7787.jpg)

### 高级链接

我们可以通过变量来设置一个链接，变量赋值在文档末尾进行：

```
这个链接用 1 作为网址变量 [Google][1]
这个链接用 runoob 作为网址变量 [Runoob][runoob]
然后在文档的结尾为变量赋值（网址）

  [1]: http://www.google.com/
  [runoob]: http://www.runoob.com/
```

显示结果如下：

![](https://hennessey02.coding.net/p/Pic/d/Pic01/git/raw/master/img//EC3ED5D2-4F0D-492A-81B3-D485623D1A9E.jpg)
