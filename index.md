---
layout: default
title: Mis notas
---

<h1>Mis notas</h1>
{% assign recent_posts = site.posts | slice: 0, 8 %}
{% if recent_posts.size > 0 %}
  <ol class="post-list">
    {% for post in recent_posts %}
      <li>
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d.%m.%Y" }}</time>
        <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
      </li>
    {% endfor %}
  </ol>
{% endif %}
