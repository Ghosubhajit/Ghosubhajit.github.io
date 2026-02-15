---
title: "Workshops and Conferences"
collection: workshops
permalink: /workshops/
layout: archive
list: hide 
---

## Upcoming & Current
*This section contains events I am attending or planning to visit.*

* 
* CMFT 2026 – [Computational Methods and Function Theory (CMFT 2026)]{https://ge.iitm.ac.in/cmft-2026}, IIT Madras, Chennai, India, December 7-11, 2026.
---
*Some nice workshops and conferences that I will probably miss.*

*

---
## 📂 Past Workshops & Seminars
*Below are details and photos from events I have participated in:*

{% for post in site.workshops reversed %}
  {% unless post.list == "hide" %}
    * [{{ post.title }}]({{ post.url }}) — *{{ post.location }}*
  {% endunless %}
{% endfor %}

<style>
  /* Keeps the page clean and removes pagination if your theme uses it */
  .pagination, .page__pagination, .pager, .page-navigation, nav.pagination {
    display: none !important;
  }
</style>
