---
title: "Workshops & Conferences"
layout: archive
permalink: /workshops/Seminars
---

## 🚀 Upcoming Events
{% assign current_date = "now" | date: "%Y-%m-%d" %}
{% assign upcoming_found = false %}

{% for event in site.workshops %}
  {% comment %} 
    If you add a 'date' field to your SCV file, 
    this logic will automatically move it.
  {% endcomment %}
  {% if event.date >= current_date %}
    ### [{{ event.title }}]({{ event.url }})
    **Location:** {{ event.location }}
    {{ event.content | strip_html | truncatewords: 30 }}
    {% assign upcoming_found = true %}
    ---
  {% endif %}
{% endfor %}

{% if upcoming_found == false %}
*No upcoming workshops at the moment.*
{% endif %}

<br>

## 📂 Past Workshops
{% for event in site.workshops %}
  {% if event.date < current_date or event.date == nil %}
    * [{{ event.title }}]({{ event.url }}) — *{{ event.location }}*
  {% endif %}
{% endfor %}

<style>
  .pagination, .page__pagination, .pager, .page-navigation, nav.pagination {
    display: none !important;
  }
</style>
