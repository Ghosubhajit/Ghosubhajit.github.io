---
title: "Workshops and Conferences"
collection: workshops
permalink: /workshops/
layout: archive
---

## 📅 Upcoming & Current
*This section contains events I am attending or planning to visit.*


---

## 📂 Past Workshops & Seminars
*Below are details and photos from events I have participated in:*

{% for post in site.workshops reversed %}
  * [{{ post.title }}]({{ post.url }}) — *{{ post.location }}*
{% endfor %}

<style>
  /* Keeps the page clean and removes pagination if your theme uses it */
  .pagination, .page__pagination, .pager, .page-navigation, nav.pagination {
    display: none !important;
  }
</style>
