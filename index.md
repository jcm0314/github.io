---
layout: home
title: 홈
---

<div class="hero-section">
  <h1 class="hero-title">안녕하세요! 👋</h1>
  <p class="hero-subtitle">개발과 기술에 대한 이야기를 나누는 공간입니다</p>
  <div class="hero-buttons">
    <a href="/about" class="btn">자세히 보기</a>
    <a href="#recent-posts" class="btn btn-outline">최근 글 보기</a>
  </div>
</div>

<section id="recent-posts" class="recent-posts">
  <h2>📝 최근 게시물</h2>
  
  <div class="posts-grid">
    {% raw %}{% for post in site.posts limit:6 %}
    <article class="post-card">
      <div class="post-category">
        {% for category in post.categories %}
        <span class="category-tag">{{ category }}</span>
        {% endfor %}
      </div>
      <h3 class="post-title">
        <a href="{{ post.url }}">{{ post.title }}</a>
      </h3>
      <div class="post-meta">
        📅 {{ post.date | date: "%Y년 %m월 %d일" }}
        {% if post.tags %}
        <span class="post-tags">
          {% for tag in post.tags %}
          #{{ tag }}
          {% endfor %}
        </span>
        {% endif %}
      </div>
      <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
      <a href="{{ post.url }}" class="btn btn-small">자세히 보기</a>
    </article>
    {% endfor %}{% endraw %}
  </div>
</section>

<section class="categories-section">
  <h2>📚 카테고리</h2>
  <div class="categories-grid">
    <a href="/categories/tech" class="category-card">
      <h3>💻 기술</h3>
      <p>새로운 기술과 도구에 대한 리뷰</p>
    </a>
    <a href="/categories/development" class="category-card">
      <h3>🔧 개발</h3>
      <p>코딩 팁과 프로젝트 후기</p>
    </a>
    <a href="/categories/daily" class="category-card">
      <h3>📖 일상</h3>
      <p>개발자의 일상과 생각들</p>
    </a>
  </div>
</section>

<section class="social-section">
  <h2>🌐 소셜 미디어</h2>
  <div class="social-links">
    <a href="https://github.com/jcm0314" class="social-link github">
      <span>GitHub</span>
    </a>
    <a href="https://twitter.com/your-twitter-username" class="social-link twitter">
      <span>Twitter</span>
    </a>
  </div>
</section> 