---
title: "标签索引"
layout: single
permalink: /tags/
author_profile: true
sidebar:
  nav: "blog"
---

## 标签云

{% for tag in site.tags %}
<span class="tag">
  <a href="{{ tag[0] | slugify | prepend: '/tags/#' | relative_url }}">
    #{{ tag[0] }}
  </a>
</span>
{% endfor %}

---

## 文章列表

{% for tag in site.tags %}
<h2 id="{{ tag[0] | slugify }}"># {{ tag[0] }}</h2>
<ul>
  {% for post in tag[1] %}
  <li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
{% endfor %}
