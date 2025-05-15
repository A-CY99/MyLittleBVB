---
layout: home
list_title: "최근 글"
---

<style>
.homepage {
  display: flex;           /* 좌우 배치 */
  align-items: flex-start; /* 상단 정렬 */
  gap: 2rem;               /* 사이 간격 */
}
.homepage .sidebar {
  width: 200px;            /* 왼쪽 카테고리 고정 너비 */
}
.homepage .main {
  flex: 1;                 /* 오른쪽 최신 글 영역 가변 */
}
</style>

<div class="homepage">

  <aside class="sidebar">
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

  <section class="main">
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
