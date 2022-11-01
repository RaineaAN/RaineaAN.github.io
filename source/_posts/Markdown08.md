---
title: Markdown 表格 (8)
date: 2021-09-24 09:57:45
categories: [学习笔记,Markdown]
tags: [Markdown学习笔记,Markdown]
index_img: https://hennessey02.coding.net/p/Pic/d/Pic01/git/raw/master/img//23EACC50-38E0-4284-B99A-6BC22E284BAC.jpg
banner_img: https://cdn.staticaly.com/gh/hennessey-v/pic@master/bg/blue-lake-v1.jpg
---

# Markdown 表格

Markdown 制作表格使用 **|** 来分隔不同的单元格，使用 **-** 来分隔表头和其他行。

语法格式如下：

```
|  表头   | 表头  |
|  ----  | ----  |
| 单元格  | 单元格 |
| 单元格  | 单元格 |
```

以上代码显示结果如下：

![](https://hennessey02.coding.net/p/Pic/d/Pic01/git/raw/master/img//23EACC50-38E0-4284-B99A-6BC22E284BAC.jpg)



对齐方式

**我们可以设置表格的对齐方式：**

- **-:** 设置内容和标题栏居右对齐。
- **:-** 设置内容和标题栏居左对齐。
- **:-:** 设置内容和标题栏居中对齐。

实例如下：

```
| 左对齐 | 右对齐 | 居中对齐 |
| :-----| ----: | :----: |
| 单元格 | 单元格 | 单元格 |
| 单元格 | 单元格 | 单元格 |
```

以上代码显示结果如下：

![](https://hennessey02.coding.net/p/Pic/d/Pic01/git/raw/master/img//87DE9D5C-44FB-4693-8735-194D3779EC3E.jpg)
