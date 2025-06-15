---
layout: archive
permalink: /categories/performance/
author_profile: true
---

{% assign posts = site.categories.performance %}
{% for post in posts %}
  {% include archive-single.html %}
{% endfor %}