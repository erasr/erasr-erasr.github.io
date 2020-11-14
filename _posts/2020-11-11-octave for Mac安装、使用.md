---
layout:     post
title:      octave for Mac安装、使用
subtitle:   安装、以及octave的基本用法
date:       2020-11-11
author:     V
header-img: img/post-bg-github-cup.jpg
catalog: true
tags:
    - 机器学习
---
#### 1、安装octave

首先，你的Mac上要安装好`Homebrew`。如果你不知道你的电脑装没装`Homebrew`，那你可以运行命令`brew -v`。如果显示下图则说明已经安装过。

![](/img/postImg/20201111_1.png)

如果没有的话，运行这条命令安装`Homebrew`。

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

也可以去[Homebrew官网](https://brew.sh)了解下。官网的介绍很明白。

下面直接运行命令`brew install octave`，然后等待安装完即可。整个安装过程可能很长，耐心。

---

#### 2、octave基本使用

[GUN Octave官网](https://www.gnu.org/software/octave/)是这么介绍的，Octave是一门专门用于科学计算编程的语言（Scientific Programming Language）。

>GUN Octave 是一门最初被发明用于数值计算的高级语言，它使用一种与Matlab几乎完全兼容的语言，为解决数字上线性和非线性问题、执行其他数值实验提供了方便的命令行界面（Command Line Interface, 简称CLI）。Octave有大量的可以用于解决常见数值线性代数问题，求解非线性方程，求得普通函数的积分，处理多项式，求得普通微分和微分代数方程积分的工具。它也非常易于通过用户用Octave自带语言编写的自定义函数，或使用由C，C++和其他语言编写的动态加载模块来进行扩展和定制。

下面介绍下octave的基本用法。

##### 2.1 基本操作

>注：一般用大写字母表示矩阵（matrix），小写字母表示向量（vector）。

`V = [1, 2 ; 3, 4]`。生成矩阵。

`V = 1 : 0.1 : 2`

`ones(2, 3)`

`zeros(2, 3)`

`rand(2, 3)`

`randn(2, 3)`

`hist(V)`

`hist(V, 50)`

`eye(4)`

`help`

##### 2.2移动数据

`size(A)`

`size(A, 1)`

`length(A)`

`load`

`who`

`whos`

`clear`

`V = priceY(1 : 10)`

`save hello.mat V`

`save hello.txt V -ascii`

`A(3, 2)`

`A(2, : )`

`A([1 3], : )`

`A( : , 2) = [10; 11; 12]`

`A[A, [100 : 200 : 300]]`

`A( : )`

`C = [A B]`

`C = [A; B]`

##### 2.3计算数据

`A * B`

`A .* B`

`A .^ B`

`1 ./ A`

`log(A)`

`exp(A)`

`abs(A)`

`-V`

`V + 1`

`A'`

`val = max(a)`

`[val, ind] = max(a)`

`max(A)`

`a < 3`

`find(a < 3)`

`[r, c] = find(A > 0.7)`

`sum(a)`

`prod(a)`

`floor(a)`

`ceil(a)`

`max(rand(3), rand(3))`

`max(A, [], 1)`

`max(max(A))`

`sum(A, 1)`

`flipud(A)`

`pinv(A)`

##### 2.4数据绘制

`plot(x, y)`

`hold on;`

`xlable('time')`

`legend('sin', cos'')`

`title('my plot')`

`print -dpng 'myplot.png'`

`close`

`figure(1); plot(t, y1);`

`subplot(1, 2, 1);`

`axis([0.5 1 -1 1])`

`clf`

`imggesc(A)`

`imagesc(A), colorbar, colormap gray;`

##### 2.5控制语句









