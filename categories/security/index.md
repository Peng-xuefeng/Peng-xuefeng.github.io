---
layout: archive
permalink: /categories/security/
author_profile: true
---

{% assign posts = site.categories.security %}
{% for post in posts %}
  {% include archive-single.html %}
{% endfor %}