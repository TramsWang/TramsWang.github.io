---
title: 杂
---

**[这里放杂文文章列表]**

<ul>
  {% for post in site.writing_essays %}
    <li>
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>