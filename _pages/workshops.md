---
title: "Workshops and Conferences"
collection: workshops
permalink: /workshops/
layout: archive
---

<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-TED2EMCK81"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-TED2EMCK81');
</script>
------------
------------


## 📅 Upcoming & Current
*This section contains events I am attending or planning to visit.*
---

### [Back to the Roots of Polynomials](https://sites.google.com/view/backtotherootsofpolynomials/main?authuser=0)

**September 22–25, 2026**  
**Paderborn University, Germany**

A workshop on zeros of polynomials and related topics.

---

### [Lectures on Probability and Stochastic Processes 2026](https://sites.google.com/view/lps-2026)

**November 30–December 5, 2026**  
**IIT Kanpur, India**

A lecture programme on probability and stochastic processes.

---

### [Computational Methods and Function Theory — CMFT 2026](https://ge.iitm.ac.in/cmft-2026)

**International Conference**  
**IIT Madras, Chennai, India**

Jointly organized by:

- Department of Mathematics, IIT Madras
- Forum d'Analystes, Chennai

---
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
