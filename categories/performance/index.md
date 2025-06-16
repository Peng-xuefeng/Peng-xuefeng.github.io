---
title: Performance Visibility
header:
  overlay_image: /assets/images/performance.jpg
  caption: "An Amazing Website"
layout: archive
permalink: /categories/performance/
author_profile: true
---

{% assign posts = site.categories.performance %}
{% for post in posts %}
  {% include archive-single.html %}
{% endfor %}