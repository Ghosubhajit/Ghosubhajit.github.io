---
title: "Miscellaneous"
collection: misc
permalink: /misc/
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

---

## 🔗 Useful Links:


1. **[Probability Events in India](https://www.isibang.ac.in/~d.yogesh/IndianProbEvent.html)**


## 📂 More

{% for post in site.misc reversed %}
  * [{{ post.title }}]({{ post.url }})
{% endfor %}

<style>
  /* Keeps the page clean and removes pagination if your theme uses it */
  .pagination, .page__pagination, .pager, .page-navigation, nav.pagination {
    display: none !important;
  }
</style>
