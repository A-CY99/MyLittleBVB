
---
layout: default    # 또는 카테고리 전용 레이아웃이 있다면 그 이름
title: "⚽️ 축구 잡설"
permalink: /categories/soccer/
---

<h1>{{ page.title }}</h1>
<ul>
{% for post in site.categories.soccer %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    <small>— {{ post.date | date: "%Y.%m.%d" }}</small>
  </li>
{% endfor %}
</ul>
