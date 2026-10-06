---
layout: prism
permalink: /blogs/
title: "Blogs"
subtitle: "Accessible write-ups of my research papers."
---

{% comment %}
  Lists every page under /blogs/. To add a post, create blogs/<slug>.md with
  layout: prism, permalink, title, order (higher = newer), venue, authors, summary.
{% endcomment %}
{% assign posts = site.pages | where_exp: "p", "p.url contains '/blogs/'" | where_exp: "p", "p.url != '/blogs/'" | sort: "order" | reverse %}
<div class="blog-list">
  {% for p in posts %}
  <a class="blog-item" href="{{ site.baseurl }}{{ p.url }}">
    <div class="blog-meta"><span class="badge badge-venue">{{ p.venue }}</span><span>{{ p.authors }}</span></div>
    <h3>{{ p.title }}</h3>
    {% if p.summary %}<p>{{ p.summary }}</p>{% endif %}
  </a>
  {% endfor %}
</div>
