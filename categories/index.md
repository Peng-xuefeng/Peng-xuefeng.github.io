---
title: "All Classes"
layout: categories
permalink: /categories/
---

<div class="grid__wrapper">
{% for category in site.categories %}
  {% assign category_name = category[0] %}
  <div class="grid__item">
    <h2 class="archive__subtitle">{{ category_name }}</h2>
    <a href="/categories/{{ category_name | slugify }}/">
      查看所有文章 ({{ category[1].size }})
    </a>
  </div>
{% endfor %}
</div>