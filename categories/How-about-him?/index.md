--- 
layout: default    # 또는 카테고리 전용 레이아웃이 있다면 그 이름
title: "이 선수는 어떤데?"
permalink: categories/How-about-him?/
--- 

<h1>{{ page.title }}</h1>
<ul>
{% for post in site.categories.How-about-him? %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <small>— {{ post.date | date: "%Y.%m.%d" }}</small>
  </li>
{% endfor %}
</ul>
