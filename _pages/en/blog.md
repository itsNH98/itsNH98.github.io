---
layout: archive
title: "Blog"
permalink: /blog/
author_profile: true
lang: en
---

Short essays on prediction markets, information economics, and market microstructure. Rigorous but (hopefully) readable.

---

{% assign posts = site.posts %}

{% for post in posts %}
  <article class="archive__item">
    <h2 class="archive__item-title" itemprop="headline">
      <a href="{{ post.url | relative_url }}" rel="permalink">{{ post.title }}</a>
    </h2>
    <p class="archive__item-excerpt">
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
      {% if post.excerpt %} &mdash; {{ post.excerpt | strip_html | truncate: 160 }}{% endif %}
    </p>
  </article>
{% endfor %}
