---
layout: page
title: Class Materials
permalink: /class_materials/
---

{% for post in site.categories.class_materials %}
  <article>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  </article>
{% endfor %}