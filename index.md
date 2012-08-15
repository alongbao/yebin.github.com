---
layout: page
title: 
description: www.yebin.info 首页 and the branch site of www.yebin.info
---
{% include JB/setup %}

<img style="width:650px;float:center" alt="Roy Flying Doctor Service 飞行演练" src="http://yebin-wordpress.stor.sinaapp.com/uploads/2012/06/rfds.jpg"/>

这里收录我的感悟。

* [主站](http://www.yebin.info)
* [Profile](https://plus.google.com/u/0/111730946330475204627/about)

感谢你的访问和留言。**Latest post: **

<ul class="posts">
  {% for post in site.posts limit:1 %}
    <li><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>