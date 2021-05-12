---
title: 小说
---

**[这里放小说文章列表]**

<ul>
  {% for post in site.writing_fictions %}
    <li>
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>