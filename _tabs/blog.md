---
layout: page
title: Blog
icon: fas fa-pen-nib
order: 5
---

{% for post in site.posts %}
  <article style="margin-bottom: 2rem;">
    <h2 style="margin-bottom: 0.25rem;">
      <a href="{{ post.url }}">{{ post.title }}</a>
    </h2>
    <small style="color: var(--text-muted-color);">
      {{ post.date | date: "%Y-%m-%d" }}
      {% if post.categories.size > 0 %} · {{ post.categories | join: ", " }}{% endif %}
    </small>
    {% if post.excerpt %}<p style="margin-top: 0.5rem;">{{ post.excerpt | strip_html | truncate: 150 }}</p>{% endif %}
  </article>
{% endfor %}
