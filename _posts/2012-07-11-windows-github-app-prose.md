---
layout: post
title: 管理 Github 的网页应用  Prose.io 
category: support
tag: [Jekyll, Prose]
description: Prose.io is a web-based interface for managing text-based content in your GitHub repositories.
published: true
---
{% include JB/setup %}
Github 的管理以前只有本地模式，和网页后台编辑内容一共两种。而 Prose.io 的出现革新地提供了网页后台新增，编辑，与删除功能。 对于 Windows 用户而言无疑是天大喜讯。

## Windows 管理 Repository 的缺陷

我和很多网络用户一样，使用 Github 上的 Jekyll 应用搭建个人网站。Rubygem 是 Jekyll 文件支持，但是其源文件却受到互联网局部屏蔽，一旦更新不全，命令 rakefile 生成和删除文件，以及切换 Jekyll 模板均失败：

	sh: git: command not found
    
对于 Mac OS，Linux 操作系统用户，解决以上错误易如反掌，而 Windows 操作用户却不得不完成复杂的设置与优化。所以，不如考虑一下 Prose.io ，每次仅管理单个文本而不会大面积破坏核心 Jekyll 。

## 什么是 Prose.io 

	Prose 提供网页后台管理 Github 知识库，能新增，编辑，删除文本文件。

看到没有？Github 自有的后台编辑功能不能新增，也不能删除。在 Prose.io 出现之前，只能通过编辑 YAML Front Matter 参数，也就是 Metadata，设定 `published: false` 关闭外部直接访问。然而文件仍然保留在知识库中，兵分真正意义的删除。

这为移动管理 Github repository 提供了选择。

## 使用 Prose.io 移动管理

个人 Notebook 和 Mac Pro 一定会不以为然，尤其那些有移动无线网络接入的电脑用家。密匙保存于本地硬盘，`rake post title="Hello World"`，接着本地服务器模式测试后 `git add .`，`git commit -a -m "update message"`，最后 `git push`。我承认，一切简单和流畅。

那么，没有笔记本电脑，四处走动又要记录一些文字，这些客户怎么办？Prose.io 目前来说是很好的选择。

* 访问 [Prose.io](http://prose.io/) 。
* 点击 Authorize with GitHub 按钮，授权访问 github 自己的帐户。有可能转向 https://github.com 完成帐户与密码输入，登入。
* 在列表中选择知识库。
* 根目录下点击 New File 或 _post 路径下 `+ NEW FILE`新增 markdown 文件。
* 预览。
* 编辑文件名，定义 Metadata，通过后台设置打开 `published: true` 或键盘开启，存盘生效。

## 其他问题

* 正文开始必须加入{% highlight php %}{/% include JB/setup %/}{% endhighlight %}
* Prose.io 的隐私和安全不全定性。
* 在 _config.yml 中设定 Prose.io 权限。
* 期望新增自动保存功能。
* 期望新增 Metadata 区浮动显示。这会对我查找 Metadata 错误警告帮助极大。

##参考

[Prose·A Content Editor for Github](http://prose.io/help/getting-started.html)

- The End -

------
