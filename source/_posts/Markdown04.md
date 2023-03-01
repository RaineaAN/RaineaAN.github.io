---
title: Markdown 区块 (4)
date: 2021-09-20 09:57:45
categories: [学习笔记,Markdown]
tags: [Markdown学习笔记,Markdown]
cover: https://hennessey02.coding.net/p/Pic/d/Pic01/git/raw/master/img//E3BF6399-6483-4C7A-8502-AE75E8D66C96.jpg
top_img: https://cdn.staticaly.com/gh/hennessey-v/pic@master/bg/blue-lake-v1.jpg 
---

# Markdown 区块

Markdown 区块引用是在段落开头使用 **>** 符号 ，然后后面紧跟一个**空格**符号：

```
> 区块引用
> 菜鸟教程
> 学的不仅是技术更是梦想
```

显示结果如下：

![](https://hennessey02.coding.net/p/Pic/d/Pic01/git/raw/master/img//DFE1124E-BC38-4C12-B7AC-053E560D4C9C.jpg)

另外区块是可以嵌套的，一个 **>** 符号是最外层，两个 **>** 符号是第一层嵌套，以此类推：

```
> 最外层
> > 第一层嵌套
> > > 第二层嵌套
```

显示结果如下：

![](https://hennessey02.coding.net/p/Pic/d/Pic01/git/raw/master/img//AA0A4A6A-33A7-48C7-971F-73FFC8FE85B0.jpg)

### 区块中使用列表

区块中使用列表实例如下：

```
> 区块中使用列表
> 1. 第一项
> 2. 第二项
> + 第一项
> + 第二项
> + 第三项
```

显示结果如下：

![](https://hennessey02.coding.net/p/Pic/d/Pic01/git/raw/master/img//E3BF6399-6483-4C7A-8502-AE75E8D66C96.jpg)

### 列表中使用区块

如果要在列表项目内放进区块，那么就需要在 **>** 前添加四个空格的缩进。

列表中使用区块实例如下：

```
* 第一项
    > 菜鸟教程
    > 学的不仅是技术更是梦想
* 第二项
```

显示结果如下：

![](https://hennessey02.coding.net/p/Pic/d/Pic01/git/raw/master/img//1B894FB4-53AC-4E2D-BA30-F4AE4DFA8B97.jpg)
