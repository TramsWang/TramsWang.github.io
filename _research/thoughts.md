---
title: 想法
---

<ul>
  {% assign sorted = site.research_thoughts | sort: 'date' | reverse %}
  {% for post in sorted %}
    <li>
      <h2>({{ post.date | date: "%Y-%m-%d" }})<a href="{{ post.url }}">{{ post.title }}</a></h2>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>