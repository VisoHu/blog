---
title: "Vim Manual"
categories:
  - Manual
tags:
  - Linux
  - Operations
---

## Diff - 文件比较
```shell
vim -d file1 file2
vimdiff file1 file2
```
--------
- 如果已经打开了文件file1，再打开另一个文件file2进行比较：
    - :vert diffsplit file2

  如果没有用vert命令，diffsplit则会分上下两个窗口。
--------
- 如果更改了某个窗口的内容，vim又没有自动更新diff检查，可以使用如下命令更新：
    - :diffupdate
--------
- 定位到不同点：
    - [c    跳到前一个不同点
    - ]c    跳到后一个不同点
--------
- 在窗口间跳转：
    - ctrl-w w    跳到下一个窗口
    - ctrl-w h    跳到左侧窗口
    - ctrl-w l    跳到右侧窗口
    - ctrl-w j    跳到下方的窗口
    - ctrl-w k    跳到上方的窗口
--------
- 合并文档：
    - dp    将差异点的当前文档内容应用到另一文档（diff put）
    - do    将差异点的另一文档的内容拷贝到当前文档（diff get）