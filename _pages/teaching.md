---
layout: archive
title: "Teaching"
permalink: /teaching/
author_profile: true
---

Here is a list of courses I have served as a TA for:

{% for post in site.teaching reversed %}
  {% include archive-single.html %}
{% endfor %}
