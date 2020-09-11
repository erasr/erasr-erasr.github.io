---
layout:     post
title:      TensorFlow使用中遇到的问题
subtitle:   TensorFlow使用中遇到的问题
date:       2020-09-11
author:     V
header-img: img/post-bg-coffee.jpeg
catalog: true
tags:
    - TensorFlow 错误集合
---

### 1. tensorflow 安装报错RuntimeError: dictionary changed size during iteration

解决方案：

vim打开报错的文件

`vim /Applications/Xcode.app/Contents/Developer/Library/Frameworks/Python3.framework/Versions/3.7/lib/python3.7/linecache.py`

找到第48行，做如下修改

`for mod in list(sys.modules.values()): # 原来是 for mod in sys.modules.values():`

因为linecache.py是只读的，所以退出vim编辑器时，采用如下命令

`:w !sudo tee %`

然后，按照操作输入密码什么的就搞定了


