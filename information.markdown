---
layout: default
title: About
permalink: /information/
---

<p>
  Category :
  {% for cat in site.categories %}
    {% assign cname = cat[0] %}
    {% assign posts_in_cat = cat[1] %}
    <a href="{{ '/categories/' | append: cname | append: '/' | relative_url }}">
      {{ cname }} ({{ posts_in_cat | size }})
    </a>{% unless forloop.last %}, {% endunless %}
  {% endfor %}
</p>