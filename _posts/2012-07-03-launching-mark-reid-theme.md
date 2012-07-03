---
layout: post
title: 转向 Mark Reid 模板
category: essay
tags: [Jekyll, SEO]
description: Mark Reid for Jekyll 模板兼容 IE6，Chrome，Opera，Firefox，Safari
published: true
---
{% include JB/setup %}

Mark Reid 是 Jekyllbootstrap 推荐的模板之一，模板兼容 IE6，Chrome，Opera，Firefox，Safari。

对 Internet Explorer 6 兼容是网站管理的重要内容。浏览器中显示支离破碎，即使内容与质量过人也将吓退网民。

IE 6.0 由 Microsoft 捆绑在操作系统内提供，2011年和 Windows XP 一起上市<sup>1</sup>。截至2012年1月，每四个中国网民中仍有一人在使用这款古董级的网页浏览工具<sup>2</sup>。

### Kill IE6

切换到 Mark Reid 模板后，所有页面在 IE6 中全部正常显示，板块和图片位置基本正常，我相信这会留住部分网页访客。不过为了提醒访客及时升级浏览器，我在页面加入了 [Kill IE6 控件](http://www.neoease.com/ie6-must-die/)。

### Time Stamp

取消日志的日期戳，改为时间戳，在日志 ..\_includes\themes\mark-reid\post.html 恰当的位置写入以下代码

	 {/{ site.time | date_to_xmlschema }/}


### 404 页面优化

Jekyllboostrap 仅仅提供了文本的 404: not found，我自己编辑了一个 404 错误的 HTML 页面。当然 Mark Reid 的 [404.html](https://github.com/mreid/mark.reid.name) 内容也可以 fork 到自己的知识栈。

### Jekyll SEO Meta 优化

* 将搜索结果指向我的 Google Plus
	
{% highlight clojure %}
 <link rel="author" href="https://plus.google.com/u/0/111730946330475204627" />
{% endhighlight %}

* 加入页面描述 Description ，内容来自于页面头部自定义 YAML 

{% highlight clojure %}
<meta name="description" content="{{page.description}}" />
{% endhighlight %}
	
* 加入页面关键词 keywords

{% highlight clojure %}
	 `{% if page.categories %}`
	 `<meta name="keywords" content="{{ page.categories }}" />`
	 {% else %}
	 <meta name="keywords" content="{{ page.tags }}" />
	 {% else %}	
	 <meta name="keywords" content="{{site.description}} />
     {% endif %}

	 {% endhighlight %}	

以上 keywords 的意义在于：

1. 如果页面已分类，使用分类词作为 seo 关键词。

1. 否则使用页面标签 Tags 作为关键词。

1. 如果页面既无分类词，同时无标签词，使用网站描述作为页面关键词。

### 小结

以上 Kill IE6 和 Jekyll SEO 均在 `..\_includes\themes\mark-reid\default.html` 完成。SEO 到底有多大作用现在还争议很大，反正各大网站都用了，我加上也不吃亏。

参考

1. [Internet Explorer历史](http://en.wikipedia.org/wiki/History_of_Internet_Explorer)

2. [IE6美国市场份额跌破1% 中国高达25.2%](http://tech.163.com/digi/12/0105/07/7N060FEJ00161MAH.html)

3. https://github.com/mreid/mark.reid.name.git

*The End*

------