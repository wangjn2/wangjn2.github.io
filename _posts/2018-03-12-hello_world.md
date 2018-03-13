---
layout: post
title: Hello World
date: 2018-03-12
tags: [Jekyll, 教程]
---

这几天有兴致研究了一些东西想更新下博客，但发现Jekyll不能运行，把过程中踩到的一些坑记录下，以便他人：

首先提示版本错误：
> zsh: /usr/local/bin/jekyll: bad interpreter: /System/Library/Frameworks/Ruby.framework/Versions/2.0/usr/bin: no such file or directory

运行 **ruby --version** 查看系统ruby版本已经升级到了2.3.3，运行命令更新jekyll和bundler，因为新版macOS */usr/bin*不能写，需要手动指定安装到*/usr/local/bin*目录
> ```bash
> sudo gem install -n /usr/local/bin jekyll bundler
> ```

<br/>

