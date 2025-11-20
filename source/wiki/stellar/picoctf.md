---
wiki: hexo-stellar 
layout: wiki
title: PicoCTF
tag: [Study,CTF]
---
### git用法

`git log`:查看上传日志

`git show`可以接分支`git branch -a`查看分支

`git checkout +commit hash`恢复

### 符号链接

`ln -s /root/flag.txt /home/player/banner`：访问 `/home/player/banner` 将会像访问 `/root/flag.txt` 一样

#### 1. `ln`：

`ln` 是用于创建链接的命令。默认情况下，`ln` 创建硬链接，但加上 `-s` 选项后，它会创建一个符号链接。

#### 2. `-s`：

`-s` 选项表示创建**符号链接**（symbolic link），也叫软链接（soft link）。符号链接类似于快捷方式，它指向另一个文件或目录。与硬链接不同，符号链接不会占用数据块，而是存储目标文件的路径。

#### 3. `/root/flag.txt`：

这是符号链接的**目标文件**。在这个例子中，`/root/flag.txt` 是目标文件，也就是你希望指向的实际文件。该文件通常是存储 "flag" 的文件，在一些挑战中，flag 是需要找到的关键文件。

#### 4. `/home/player/banner`：

这是**符号链接的路径和名称**。`/home/player/banner` 是你希望创建的符号链接的路径和名称。通过这个符号链接，用户可以访问 `/root/flag.txt` 文件，而无需直接访问原文件路径。

#### 总结：

这个命令创建了一个符号链接 `banner`，它位于 `/home/player/` 目录，指向 `/root/flag.txt` 文件。换句话说，访问 `/home/player/banner` 将会像访问 `/root/flag.txt` 一样，返回相同的内容。

### root权限shell

#### `sudo -l`:查看当前用户可用权限，如需要从vim得到root，`sudo vi`然后`:!sh`进入root权限

### 如何自动执行任务以在 Linux 服务器上间隔运行？

#### `/etc/crontab`

### man命令，（如果直接加脚本名或许...

通过 man 命令，您可以获取关于特定命令或主题的详细信息。

#### 语法

```
man [选项] [节号] 命令/主题
```

一些常见的选项包括：

- `-f`：显示与指定关键字相关的手册页面。
- `-k`：搜索手册页中与关键字匹配的条目。
- `-a`：显示所有匹配的手册页面。
- `-w`：仅显示手册页的位置，而不显示其内容。