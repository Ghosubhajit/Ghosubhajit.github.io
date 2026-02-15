---
title: "Seminars & Workshops"
layout: archive
permalink: /seminars-hub/
---

## 🟢 Upcoming & Ongoing
{% assign current_date = "now" | date: "%Y-%m-%d" %}
{% assign upcoming_count = 0 %}

{% comment %} 
Change 'site.posts' to 'site.seminars' or 'site.workshops' 
depending on what you named your folder 
{% endcomment %}

{% for item in site.seminars %}
  {% if item.date >= current_date %}
    ### [{{ item.title }}]({{ item.url }})
    **Date:** {{ item.date | date: "%B %d, %Y" }}  
    *{{ item.description }}*
    
    [View Details & Abstract]({{ item.url }})
    ---
    {% assign upcoming_count = upcoming_count | plus: 1 %}
  {% endif %}
{% endfor %}

{% if upcoming_count == 0 %}
*No upcoming events currently scheduled.*
{% endif %}

<br>

## 📜 Past Events
Below are the links to my previous seminars and workshops:

{% for item in site.seminars reversed %}
  {% if item.date < current_date %}
    * {{ item.date | date: "%Y" }}: [{{ item.title }}]({{ item.url }})
  {% endif %}
{% endfor %}

<style>
  .pagination, .page__pagination, .pager, .page-navigation, nav.pagination {
    display: none !important;
  }
</style>
