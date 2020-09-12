---
layout:     post
title:      Mac使用Timemachine自动备份
subtitle:   Timemachine谁用谁知道
date:       2020-09-11
author:     V
header-img: img/post-bg-keybord.jpg
catalog: true
tags:
    - Mac
---

#### 引言

我相信很多人都有丢失文件的经历，然后想尽各种办法找回数据。与其等到真的意外丢失文件了再着急，不如从现在开始，养成随时备份的好习惯。

Timemachine你值得一试。

#### 1. 选择硬盘

首先，我们需要一块移动硬盘。我直接用的是在老电脑上卸下来的，500GB。然后在网上买了个透明的硬盘盒。如果没有老电脑可以拆，在网上买块新的也行。

![](/img/Timemachine/1.jpeg)

**[透明移动硬盘盒（点我购买）](https://union-click.jd.com/jdc?e=&p=AyIGZRtfEAQTBVwdWh0yFgBSHV4UBhQAUhJrUV1KWQorAlBHU0VeBUVNR0ZbSkdETlcNVQtHRVNSUVNLXANBRA1XB14DS10cQQVYD21XHgNSHF0QAxYBUhxSJXxqfCVIC3AAdwFPcyx2fRJkIU1BfUQeC2UaaxUDEwRWHVgRChs3ZRtcJUN8B1QaWRcBFgZlGmsVBhoPXB1SFQUVA1ceaxICGzdVH1wRABcGXBtdFGxTRAcrayUBIjdlG2sWMlBpVxxcFgVGBlRLXkECFwFRHVIVBkJUBh5dRwMaDlVJCBAyEAZUH1I%3D)**

#### 2. 初始化硬盘

准备好硬盘后，下边要对硬盘进行初始化。

打开系统自带的「磁盘工具」，在左侧选中自己的硬盘，点击上方的「抹掉」。在弹出的对话框中，名称自己随便设置一个，格式选择「Mac OS 扩展（区分大小写 日志式）」（默认项）。最后点击「抹掉」，等待完成。

![](/img/Timemachine/2.png)

**建议让Timemachine独占硬盘**

#### 3. 加密磁盘

当做完上述步骤后，Mac会自动提示你是否使用该硬盘对Mac备份。为了数据的安全性，建议在弹出的对话框中勾选「给备份磁盘加密」。

在弹出的对话框中输入密码和提示信息即可。

![](/img/Timemachine/4.png)

这个加密过程是非常缓慢的，加密速度大概在20~30MB之间。如果加密100GB的数据，大概耗时1小时左右。不过，加密过程可以中断，你可以把硬盘推出，等下次你再接上硬盘的时候，Mac会自动进行上次未完成的加密。

#### 4. 排除

我们还可以根据自己的需求选择不需要备份的文件。

打开时间机器-》选项，将不需要备份的文件添加上去。





