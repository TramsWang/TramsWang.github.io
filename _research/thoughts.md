---
title: 想法
---

<ul>
  {% for post in site.research_thoughts %}
    <li>
      <h2>({{ post.date | date: "%Y-%m-%d" }})<a href="{{ post.url }}">{{ post.title }}</a></h2>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>