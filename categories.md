---
title: "分类目录"
layout: single
permalink: /categories/
author_profile: true
sidebar:
  nav: "blog"
---

## 分类列表

{% for category in site.categories %}
<h2 id="{{ category[0] | slugify }}">{{ category[0] }}</h2>
<ul>
  {% for post in category[1] %}
  <li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
{% endfor %}
