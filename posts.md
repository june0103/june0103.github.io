---
title: 글 목록
nav_order: 1
---

# 글 목록

{% for post in site.posts %}
[{{ post.title }}]({{ post.url | relative_url }}) — {{ post.date | date: "%Y-%m-%d" }}
{% endfor %}
