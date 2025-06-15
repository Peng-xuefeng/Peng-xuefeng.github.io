---
layout: archive
permalink: /categories/functional/
author_profile: true
---

{% assign posts = site.categories.functional %}
{% for post in posts %}
  {% include archive-single.html %}
{% endfor %}