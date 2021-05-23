---
title: 诗词
---

<ul>
  {% assign sorted = site.writing_poetry | sort: 'date' | reverse %}
  {% for post in sorted %}
    <li>
      <h2>({{ post.date | date: "%Y-%m-%d" }})<a href="{{ post.url }}">{{ post.title }}</a></h2>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>