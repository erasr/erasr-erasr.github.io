---
layout:     post
title:      Matplotlib的常见用法
subtitle:   Matplotlib的常见用法
date:       2020-11-18 
author:     V
header-img: img/post-bg-github-cup.jpg
catalog: true
tags:
    - Python
---

### 1.plt.subplots()

返回一个包含figure和axes对象的元组。因此，通常使用`fig,ax = plt.subplots()`将元组分解为fig和ax两个变量。

首先我们先介绍下Figure、Axes和Axis吧。具体区别看下官方的图。

![图片来源[matplotlib](https://matplotlib.org/1.5.1/faq/usage_faq.html#parts-of-a-figure)](/img/postImg/20201117_2.png)

Figure是整个「画板」，也就是红色的框。在上边可以画多个图像（Axes），也就是蓝色的框。而蓝色的框才是具体的坐标轴（Axis）。

Axes是Axis的复数，Axes在这里指的是一套坐标轴，而Axis才是指的具体单个坐标轴。何为「一套坐标轴」、「单个坐标轴」呢？有人这么说：

>Axis 指 x、y 坐标轴等（如果有三维那就还有 z 轴），代表的是 “坐标轴”。而 Axes 在英文里是 Axis 的复数形式，也就是说 axes 代表的其实是 figure 当中的一套坐标轴。之所以说一套而不是两个坐标轴，是因为如果你画三维的图，axes 就代表 3 根坐标轴了。所以，在一个 figure 当中，每添加一次 subplot ，其实就是添加了一套坐标轴，也就是添加了一个 axes，放在二维坐标里就是你添加了两根坐标轴，分别是 x 轴和 y 轴。所以当你只画一个图的时候，plt.xxx 与 ax.xxx 其实都是作用在相同的图上的。

为了加深理解，再看一个图。

![](/img/postImg/20201117_2.png)

值得注意的是，当只有一个Axes时，`plt.plot() `和 `ax.plot()` 是作用在同一张图上。





