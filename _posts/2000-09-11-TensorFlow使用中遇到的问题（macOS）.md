---
layout:     post
title:      TensorFlow使用中遇到的问题（macOS）
subtitle:   将遇到的错误整理一下
date:       2020-09-11
author:     V
header-img: img/post-bg-keybord.jpg
catalog: true
tags:
    - TensorFlow 错误集合 Mac
---

### 1. TensorFlow安装报错RuntimeError: dictionary changed size during iteration

>TensorFlow版本：1.15.3
>
>Python版本 ：3.7.3
>
>macOS版本：10.15.6

解决方案：

vim打开报错的文件

`vim /Applications/Xcode.app/Contents/Developer/Library/Frameworks/Python3.framework/Versions/3.7/lib/python3.7/linecache.py`

找到第48行，做如下修改

`for mod in list(sys.modules.values()): # 原来是 for mod in sys.modules.values():`

因为linecache.py是只读的，所以退出vim编辑器时，需采用强制保存命令

`:w !sudo tee %`

然后，输入密码

```
W12: Warning: File "/etc/hosts" has changed and the buffer was changed in Vim as well
See ":help W12" for more info.
[O]K, (L)oad File:
```

这里按`L`即可，表示重新载入文件

至此，搞定

---


