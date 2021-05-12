---
title: 想法
---

**[这里列举所有想法的文章列表]12**

<ul>
  {% for post in site.research_thoughts %}
    <li>
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>