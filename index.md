---
layout: page
title: Greeting
description: www.yebin.info 首页
---
{% include JB/setup %}

<img src="http://yebin-wordpress.stor.sinaapp.com/uploads/2012/06/rfds.jpg" style="width:650px;float:center" alt="Roy Flying Doctor Service 飞行演练"></a>

这里是叶斌的个人网站。这里收录了我的随想，和职业感悟。

* [Profile](https://plus.google.com/u/0/111730946330475204627/about "叶斌的简介")

* [备用网站](http://calepin.yebin.info "本站受屏蔽时请访问 blogspot")

* [联系](http://www.google.com/recaptcha/mailhide/d?k=01pQWqEBdhPafoq8zGW2d99w==&c=V3fz3TZK9GkOgTUi5fXexp9i_NzeIefH8cbCepHNwe0= "加密的邮箱地址")

感谢你的访问和留言。


### 日志
<ul class="posts">
  {% for post in site.posts limit:1 %}
    <li><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>