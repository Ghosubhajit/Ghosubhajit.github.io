---
title: "Teaching"
layout: archive
permalink: /teaching/
---

## 📖 Current Teaching
*Courses I am currently instructing or TA-ing.*

{% assign current_date = "now" | date: "%Y-%m-%d" %}
{% assign active_teaching = false %}

{% for course in site.teaching %}
  {% if course.active == true %}
    ### [{{ course.title }}]({{ course.url | relative_url }})
    **Role:** {{ course.role }} | **Institution:** {{ course.location }}
    
    {{ course.description }}
    {% assign active_teaching = true %}
    ---
  {% endif %}
{% endfor %}

{% if active_teaching == false %}
*No active courses at the moment.*
{% endif %}

<br>

## 📚 Past Teaching Archive
*Previous courses, tutorials, and grading responsibilities.*

{% for course in site.teaching %}
  * [{{ course.title | default: "Untitled Course" }}]({{ course.url | relative_url }}) — {{ course.location }}
{% endfor %}
<style>
  .pagination, .page__pagination, .pager, .page-navigation, nav.pagination {
    display: none !important;
  }
</style>
