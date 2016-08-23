---
title: Git快速入门
date: 2016-08-12 15:33:45
tags: [Git]
---

By lxl

------

> Git 快速入门，为完全不了解 Git 的同为小白的我们，快速了解 Git

------

## Git 基本知识
- Git 是什么？和 SVN有什么区别？
SVN、CVS都是集中式版本控制系统，而 Git 是分布式版本控制系统。
集中式和分布式的区别在于：集中式的意思是，有一台中央服务器，大家各自的电脑的版本库（repository）都是从中央服务器下下来的，因此都公用同一个版本库，因此当中央服务器出了问题，所有人都没法干活了。
而像Git 这样分布式版本控制系统，每个人的电脑都有完整的版本库，只要把各自修改的文件提交给对方便可，但其实为了方便，Git 也是有中央服务器的，也就是 Github上（中央服务器）的远程仓库（remote repository）。

## Git 立即上手，
- 上 Github 网站 注册一个账号
- 理解 Repository（仓库）、branch（分支）的概念。我建议大家跟着Github网站首页上的[“Read the guid”](https://guides.github.com/activities/hello-world/)的文档操作一遍，
- 安装 Git，下载好了 Git 之后会有一个软件 Git bash，点击鼠标右键就会看到“ Git Bash Here”了
- 配置账号信息($ 不用输入),自报家门，因为每个人都有版本库，因此必须说明你的名字和Email地址
`````
$ git config --global user.name "yourName" # yourName是你自己的名字，可以随便输
$ git config --global user.email "email@example.com"  
`````
- 创建 SSH key，因为 Git 仓库 和 Github 仓库之间的传输时通过 SSH 加密的，不能什么人都往自己的远程仓库上添加修改代码不是嘛。所以， Github 上需要保存你电脑生成的 SSH key，那么跟着GitHub上的教程 [Generating an SSH key](https://help.github.com/articles/generating-an-ssh-key/) 走就行了
- 在上面的步骤下有了自己的 Repository上，将 Github上的远程仓库（remote repo）clone（克隆）到本地 ，用下来的命令 *git clone [git address]*，[git address]换成你在第2步创建的仓库（repo）地址 
``````
$ git clone [Git address]
``````
- 克隆到本地电脑下了后呢，想要修改/添加一些地方到 GitHub 上的远程仓库，比如你本地添加了 text.txt 之后，想要添加到 Github 上的远程仓库，那么需要三步，*git add .*、*git commit -m "注释内容"*、*git push*（要想具体了解的话，下面有说到详细教程，强烈建议跟着下面的教程学Git，而不是快速入门）
``````
$ git add .  # git add . 是把和远程仓库不一样的文件全部提交上去
$ git commit -m "test"
$ git push
``````
<span style="color:red;">最好的方式是先创建远程库，然后，从远程库克隆，接着在本地修改后提交到远程库。别问我为什么，这么做就对了


## 详细教程
- [廖雪峰的Git教程](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/001373962845513aefd77a99f4145f0a2c7a7ca057e7570000) 
<span style="color:red;">强烈建议跟着廖老师的教程学Git，简单易懂，看完就不用再找教程、博客了</span>
- [阮一峰的常用 Git 命令清单](http://www.ruanyifeng.com/blog/2015/12/git-cheat-sheet.html)
- [大神写的‘我的Git笔记’](http://yanhaijing.com/git/2014/11/01/my-git-note/)