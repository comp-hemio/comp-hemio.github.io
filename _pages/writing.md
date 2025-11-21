---
layout: archive
title: "Writing"
permalink: /writing/
author_profile: true
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/writing-header.jpg
---

## Compositional Essays & Reflections

Analytical essays about music, composition, and the philosophical questions that emerge through the creative process.

Each piece in the Hemio Monthly Series is accompanied by an essay exploring its musical structure, compositional choices, and deeper meaning.

---

{% for post in site.posts %}
  <article class="archive__item">
    <h2 class="archive__item-title">
      <a href="{{ post.url }}">{{ post.title }}</a>
    </h2>
    <p class="page__meta">{{ post.date | date: "%B %d, %Y" }}</p>
    {% if post.excerpt %}
      <p class="archive__item-excerpt">{{ post.excerpt }}</p>
    {% endif %}
  </article>
{% endfor %}
