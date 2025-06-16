---
title: Auto-Calc Coverage
header:
  overlay_image: /assets/images/elevator.jpg
  caption: "An Amazing Website"
layout: archive
permalink: /categories/automation/
author_profile: true
---

{% assign posts = site.categories.automation %}
{% for post in posts %}
  {% include archive-single.html %}
{% endfor %}