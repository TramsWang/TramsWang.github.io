---
title: 诗词
---

**[这里放诗词文章列表]**

<ul>
  {% for post in site.writing_poetry %}
    <li>
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>