---
layout: page
title: Greeting
description: www.yebin.info 首页
---
{% include JB/setup %}

<img src="http://yebin-wordpress.stor.sinaapp.com/uploads/2012/06/rfds.jpg" style="width:650px;float:center" alt="Roy Flying Doctor Service 飞行演练"></a>

这里是叶斌的个人网站。这里收录了我的随想，和职业感悟。

<table align="center">
<tbody>
<tr>
<td width=200px><a href="http://calepin.yebin.info" title="本站受屏蔽时请访问 blogspot">备用网站</a></td>
<td width=200px><a href="https://plus.google.com/u/0/111730946330475204627/about" title=""叶斌的简介"">Profile</a></td>
</tr>
</tbody>
</table>

感谢你的访问和留言。


**Latest Blog**
<ul class="posts">
  {% for post in site.posts limit:1 %}
    <li><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>