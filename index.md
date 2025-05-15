---
layout: home
list_title: "최근 글"
---

<style>
.homepage {
  display: flex;
}
/* sidebar를 뷰포트 왼쪽에 고정 */
.homepage .sidebar {
  position: fixed;
  top: 4rem;        /* 헤더 높이에 맞춰 조정 */
  left: 0;
  width: 200px;     /* 원하는 고정 폭 */
}
/* main은 sidebar 너비만큼 오른쪽으로 띄우기 */
.homepage .main {
  margin-left: 220px;  /* sidebar width + gap */
  flex: 1;
}
</style>


<div class="homepage">
  <aside class="sidebar">…</aside>
    <h2>카테고리</h2>
    <ul>
      <li><a href="/categories/soccer">⚽️ 축구 잡설</a></li>
      <li><a href="/categories/2425-reviews">24/25 경기 후기</a></li>
      <li><a href="/categories/How-about-him?">이 선수는 어떤데?</a></li>
      <details>
        <summary>📂 과거 시즌들</summary>
        <ul>
          <li><a href="/categories/2324-reviews">23/24 경기 후기</a></li>
          <li><a href="/categories/ancient-reviews">고대 경기들 후기</a></li>
        </ul>
      </details>
    </ul>
  </aside>

  <section class="main">…</section>
    <h2>{{ page.list_title }}</h2>
    <ul>
      {% for post in site.posts %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
        <small>— {{ post.date | date: "%Y.%m.%d" }}</small>
      </li>
      {% endfor %}
    </ul>
  </section>

</div>
