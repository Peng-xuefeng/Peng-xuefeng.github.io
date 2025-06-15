---
layout: archive
header:
  overlay_image: /assets/images/about.jpg
  caption: "An Amazing Website"
permalink: /categories/about/
author_profile: true
---

{% assign posts = site.categories.about %}
{% for post in posts %}
  {% include archive-single.html %}
{% endfor %}