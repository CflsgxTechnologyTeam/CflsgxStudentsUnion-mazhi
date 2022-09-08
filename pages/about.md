---
layout: page
title: About
description: 关于本站
keywords: 关于, 成外高新
comments: true
menu: 关于
permalink: /about/
---

# 关于团学会

## 我们
成都外国语学校高新校区团学会是学校党委领导和团委指导下的主要学生组织，是学生与学校沟通、联系的桥梁和纽带。成外高新团学会以“从同学中来，到同学中去，为同学服务，对同学负责”为行动准则，自主开展工作，致力于丰富同学课余文化生活，助力完善校园管理机制。  
团学会积极促进同学全面成长进步、培养优良学风，收集同学学业发展、身心健康、社会融入、权益维护等方面的需求和困难，并及时反馈学校，帮助有效解决。  
团学会是现在学校中的组织结构之一，是学生自己的群众性组织，是学校联系学生的桥梁和纽带，是每个学校不可缺少的部门。它是提倡自我服务，自我管理，自我学习的学生组织，为学校学生和老师提供无偿服务的部门。引导同学努力做到身体好、学习好、工作好，德、智、体、美、劳全面发展，成为有社会主义觉悟的、有科学文化知识的、身体健康的人。  
[![第五届团学会合影](/images/about/picbg.webp)](https://v1.cflsgx.top/images/picbg.jpg)  

## 构成
{% for skill in site.data.skills %}
### {{ skill.name }}
<div class="btn-inline">
{% for keyword in skill.keywords %}
<button class="btn btn-outline" type="button">{{ keyword }}</button>
{% endfor %}
</div>
{% endfor %}

# 关于本站

## 站点内容与管理
本站所属组织为成都外国语学校高新校区团学会,用于展示团学会动态及学生活动风采。本站由团学会自行运营，其内容与成外高新无直接关系。
本站建立初衷是为了给团学会一个展示自我对外交流的平台，不会用于其他用途。

## 贡献  
网站建设：高2020级3班 邹怡翔  
团学会LOGO设计：高2021级2班 康雯雯

## 联系我们
<ul>
{% for website in site.data.social %}
<li>{{website.sitename }}：<a href="{{ website.url }}" target="_blank">@{{ website.name }}</a></li>
{% endfor %}
</ul>  

