---
layout: page
title: About
description: 关于本站
keywords: 关于, 成外高新
comments: true
menu: 关于
permalink: /about/
---

## 站点内容与管理
本站所属组织为成都外国语学校高新校区团学会,用于展示团学会动态及学生活动风采。本站由团学会自行运营，其内容与成外高新无直接关系。
本站建立初衷是为了给团学会一个展示自我对外交流的平台，不会用于其他用途。

## 联系

<ul>
{% for website in site.data.social %}
<li>{{website.sitename }}：<a href="{{ website.url }}" target="_blank">@{{ website.name }}</a></li>
{% endfor %}
</ul>  

## 构成

{% for skill in site.data.skills %}
### {{ skill.name }}
<div class="btn-inline">
{% for keyword in skill.keywords %}
<button class="btn btn-outline" type="button">{{ keyword }}</button>
{% endfor %}
</div>
{% endfor %}
