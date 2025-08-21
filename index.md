---
layout: default
title: 首頁
---

<h1>{{ site.title }}</h1>
<p>{{ site.description }}</p>

<ul>
  {% for post in paginator.posts %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> <small>{{ post.date | date: "%Y-%m-%d" }}</small></li>
  {% endfor %}
</ul>

{% if paginator.total_pages > 1 %}
<nav>
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path | relative_url }}">&laquo; 上一頁</a>
  {% endif %}
  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path | relative_url }}">下一頁 &raquo;</a>
  {% endif %}
</nav>
{% endif %}
