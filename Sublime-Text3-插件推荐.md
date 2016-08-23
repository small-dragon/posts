---
title: Sublime Text3 插件推荐
date: 2016-08-17 16:43:10
tags: [tools]
---

By lxl

------

> ST3 插件个人推荐，包含文档、设置，为小白准备

------

## 安装和破解
- 首先上 [官网](http://www.sublimetext.com/3) 下载相应版本最新的`ST3`
- 破解注册码，我自己找了一个 [注册码](http://blog.sina.com.cn/s/blog_7f5571aa0102w3xq.html)
- 安装 `package control`（安装package control之后才能安装其他插件）
使用Ctrl+`快捷键或者通过View->Show Console菜单打开命令行，粘贴如下代码：
``````
import urllib.request,os; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read())
``````
- 安装插件 ctrl + shift + p -> install package -> 输入你想安装的插件名 -> enter

## 推荐插件
- less：`less` 文件高亮
- CTags：函数跳转，Alt + 点击函数名，跳到对应函数
- Emmets：快速编写 HTML 文件插件，安装之后，尝试输入 `div>a>span` 之后按 Tab键即可看到效果
- [better-completion](https://github.com/Pleasurazy/Sublime-Better-Completion)：可以提供 `Javascirpt/jQuery`、`html`、`Bootstrap`等等 代码提示的插件 需要修改配置，preferences-> package-settings-> sublime-better-completion->setting-user）
  需要把setting-default默认的复制到setting-user，然后修改false的为true就可以了
- sibarEnhancement：安装之后点击右键在左边栏和代码区即可看到增强的功能，比如打开所在文件的文件夹、在浏览器中打开文件等等
- colorhighlighter：颜色高亮插件[colorhighlighter](https://github.com/Monnoroch/ColorHighlighter)，在CSS、less、sass等文件中，只要是颜色属性，都能以高亮的方式显示，另外按 `shift + ctrl + c` 会弹出调色盘，比起 `colorPicker` 插件打开时的慢、卡顿，这个插件明显简洁很多
另外，高亮的方式有多种，我这边的设置如下（Preference -> Package Setting -> Color Highlighter -> Setting-User）：
````
{
    "ha_style": "filled",
    "ha_icons": true,
}

````
配置的效果如图，前提是安装了 [ImageMagick](http://www.imagemagick.org/script/binary-releases.php)，不是 ST 插件包，是一个软件安装包
![colorhighlighter](https://camo.githubusercontent.com/e13f5346a650e7e3fc2269fd4de3904d78c8fd1e/687474703a2f2f692e696d6775722e636f6d2f55506d456b30392e706e67)

- terminal：输入 `terminal` 的第一个控制台插件，非常方便，安装之后在想要打开的文件上点击右键即可发现多了一个 *open terminal here*，就不用在 `cmd`  上输入文件的地址了
但还需要在相对应的'Setting-User'上配置才能出现黑色的 `cmd` 而不是蓝色的 `cmd` ，*"C:\\Windows\\System32\\cmd.exe"* 为你的 `cmd` 文件地址
`````
{
  // Replace with your own path to cmder.exe
  "terminal": "C:\\Windows\\System32\\cmd.exe",
  "parameters": ["/START", "%CWD%"]
}
`````
- markdown Editing：`markdown` 语法高亮
- OmnimarkupPreviwer：在浏览器上预览效果，快捷键为 `ctrl + alt + o` 
- DocBlockr：JS等代码的注释插件 [DocBlockr](https://github.com/spadgos/sublime-jsdocs)，输入 `/**`，再按 `tab` 即可触发，`CSS`文件不能触发

## 结束语
好了，赶紧去配置属于自己的 `Sublime Text3` 吧
