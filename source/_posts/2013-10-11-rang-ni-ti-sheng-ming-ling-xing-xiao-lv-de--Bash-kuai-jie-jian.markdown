---
layout: post
title: 让你提升命令行效率的 Bash 快捷键
date: 2013-10-11 16:56:18
comments: true
categories: [bash,bi,linux,mac,html]
---
## 查看`bash`版本

生活在 Bash shell 中，熟记以下快捷键，将极大的提高你的命令行操作效率。

查看你`Linux`系统中的`bash`版本。

    [root@allentest solife]# echo $SHELL
    /bin/bash
    [root@allentest solife]# which bash
    /bin/bash
    [root@allentest solife]# whereis bash
    bash: /bin/bash /usr/share/man/man1/bash.1.gz
    [root@allentest solife]# 

## 编辑命令

| 组合键 | 效果 |
|--------|------|
   |  Ctrl + a | 移到命令行首  
   |  Ctrl + e | 移到命令行尾
   | Ctrl + f | 按字符前移（右向）
   | Ctrl + b | 按字符后移（左向）
   | Alt + f | 按单词前移（右向）
   | Alt + b | 按单词后移（左向）
   | Ctrl + xx | 在命令行首和光标之间移动
   | Ctrl + u | 从光标处删除至命令行首
   | Ctrl + k  | 从光标处删除至命令行尾
   | Ctrl + w | 从光标处删除至字首
   | Alt + d | 从光标处删除至字尾
   | Ctrl + d | 删除光标处的字符
   | Ctrl + h | 删除光标前的字符
   | Ctrl + y | 粘贴至光标后
   | Alt + c | 从光标处更改为首字母大写的单词
   | Alt + u | 从光标处更改为全部大写的单词
   | Alt + l | 从光标处更改为全部小写的单词
   | Ctrl + t | 交换光标处和之前的字符
   | Alt + t | 交换光标处和之前的单词
   | Alt + Backspace| 与 Ctrl + w 相同类似，分隔符有些差别 [感谢 rezilla 指正]

## 操作历史命令

| 组合键 | 效果 |
|--------|------|
   |  Ctrl + r | 逆向搜索命令历史
   |  Ctrl + g | 从历史搜索模式退出
   |  Ctrl + p |  历史中的上一条命令
   |  Ctrl + n |  历史中的下一条命令
   |  Alt + `.`|  使用上一条命令的最后一个参数

## 控制命令

| 组合键 | 效果 |
|--------|------|
     | Ctrl + l | 清屏
     | Ctrl + o | 执行当前命令，并选择上一条命令
     | Ctrl + s | 阻止屏幕输出
     | Ctrl + q | 允许屏幕输出
     | Ctrl + c | 终止命令
     | Ctrl + z | 挂起命令

## `!` 命令

| 组合键 | 效果 |
|--------|------|
     | !! | 执行上一条命令
     | !blah | 执行最近的以 blah 开头的命令，如 !ls
     | !blah:p | 仅打印输出，而不执行
     | !$ | 上一条命令的最后一个参数，与 Alt + . 相同
     | !$:p | 打印输出 !$ 的内容
    |  !* | 上一条命令的所有参数
     | !*:p | 打印输出 !* 的内容
     | ^blah | 删除上一条命令中的 blah
     | ^blah^foo | 将上一条命令中的 blah 替换为 foo
     | ^blah^foo^ | 将上一条命令中所有的 blah 都替换为 foo

友情提示：

以上介绍的大多数 Bash 快捷键仅当在 emacs 编辑模式时有效，若你将 Bash 配置为 vi 编辑模式，那将遵循 vi 的按键绑定。Bash 默认为 emacs 编辑模式。如果你的 Bash 不在 emacs 编辑模式，可通过 set -o emacs 设置。

^S、^Q、^C、^Z 是由终端设备处理的，可用 stty 命令设置。
    
## 参考

[让你提升命令行效率的 Bash 快捷键 [完整版]](http://linuxtoy.org/archives/bash-shortcuts.html)
