---
title: "Teaching"
layout: archive
permalink: /teaching/
---

## 📖 Current
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
*No active TA or Teaching at the moment.*
{% endif %}

## 📁 Past Teaching Archive

{% assign past_courses = site.teaching | where_exp: "item", "item.active != true" %}
{% assign teaching_groups = past_courses | group_by: "venue" %}

{% for group in teaching_groups %}
  <div style="margin-top: 30px;">
    <h3 style="border-bottom: 1px solid #eee; padding-bottom: 5px;">{{ group.name | default: "Other Institutions" }}</h3>
    <ul style="list-style-type: none; padding-left: 10px;">
      {% for course in group.items %}
        <li style="margin-bottom: 8px;">
          <strong><a href="{{ course.url | relative_url }}">{{ course.title }}</a></strong> — 
          <em>{{ course.type }} ({{ course.date | date: "%Y" }})</em>
        </li>
      {% endfor %}
    </ul>
  </div>
{% endfor %}
<style>
  .pagination, .page__pagination, .pager, .page-navigation, nav.pagination {
    display: none !important;
  }
</style>
