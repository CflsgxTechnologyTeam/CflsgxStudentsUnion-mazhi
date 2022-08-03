---
layout: page
title: Links
description: 友情链接
keywords: 友情链接
comments: true
menu: 链接
permalink: /links/
---

> 官方的

<ul>
{% for link in site.data.links %}
  {% if link.src == 'official' %}
  <li><a href="{{ link.url }}" target="_blank">{{ link.name}}</a></li>
  {% endif %}
{% endfor %}
</ul>

> 个人的

<ul>
{% for link in site.data.links %}
  {% if link.src == 'personal' %}
  <li><a href="{{ link.url }}" target="_blank">{{ link.name}}</a></li>
  {% endif %}
{% endfor %}
</ul>
