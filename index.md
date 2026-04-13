---
layout: default
title: "홈"
---
<section class="hero">
  <div class="container">
    <span class="hero-badge">Welcome to zzhining</span>
    <h1 class="hero-title">
      배우고, 기록하고,<br><em>함께 성장하는</em> 공간
    </h1>
    <p class="hero-desc">
      생성형 AI, 데이터 분석, 머신러닝 등 다양한 지식을 기록하고 나눕니다.
    </p>
    <div class="hero-actions">
      <a href="/theory/" class="btn btn-primary">지식창고 둘러보기</a>
      <a href="/blog/" class="btn btn-outline">블로그 읽기</a>
    </div>
  </div>
</section>

<div class="container">

  <!-- 최근 블로그 -->
  <section class="section">
    <div class="section-header">
      <h2 class="section-title">최근 블로그</h2>
      <a href="/blog/" class="section-link">전체 보기 →</a>
    </div>
    <div class="posts-grid">
      {% for post in site.posts limit:3 %}
      <article class="post-card">
        <div class="post-card-body">
          {% if post.category %}
          <span class="post-card-category">{{ post.category }}</span>
          {% endif %}
          <h3 class="post-card-title">
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </h3>
          <p class="post-card-excerpt">{{ post.excerpt | strip_html | truncate: 100 }}</p>
          <div class="post-card-meta">
            <span class="post-card-date">
              <svg viewBox="0 0 16 16" width="12" height="12" fill="currentColor"><path d="M3.5 0a.5.5 0 0 1 .5.5V1h8V.5a.5.5 0 0 1 1 0V1h1a2 2 0 0 1 2 2v11a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V3a2 2 0 0 1 2-2h1V.5a.5.5 0 0 1 .5-.5zM1 4v10a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1V4H1z"/></svg>
              {{ post.date | date: "%Y.%m.%d" }}
            </span>
            <a href="{{ post.url | relative_url }}" class="post-card-link">읽기 →</a>
          </div>
        </div>
      </article>
      {% else %}
      <div class="empty-state"><p>아직 작성된 블로그 포스트가 없습니다.</p></div>
      {% endfor %}
    </div>
  </section>

  <!-- 지식창고 -->
  <section class="section" style="border-top: 1px solid var(--border); padding-top: 60px;">
    <div class="section-header">
      <h2 class="section-title">지식창고</h2>
      <a href="/theory/" class="section-link">전체 보기 →</a>
    </div>
    <div class="theory-grid">
      <div class="theory-card">
        <div class="theory-card-icon">🤖</div>
        <h3 class="theory-card-title"><a href="/theory/generative-ai/">생성형 AI</a></h3>
        <p class="theory-card-desc">ChatGPT, Claude, Gemini 등 생성형 AI 기술과 활용법</p>
      </div>
      <div class="theory-card">
        <div class="theory-card-icon">🐍</div>
        <h3 class="theory-card-title"><a href="/theory/python-basics/">파이썬 기초</a></h3>
        <p class="theory-card-desc">Python 문법, 자료구조, 함수, 클래스 등 기초 개념</p>
      </div>
      <div class="theory-card">
        <div class="theory-card-icon">📊</div>
        <h3 class="theory-card-title"><a href="/theory/data-analysis/">데이터 분석</a></h3>
        <p class="theory-card-desc">Pandas, NumPy, 통계 분석, EDA 등 데이터 분석 기법</p>
      </div>
      <div class="theory-card">
        <div class="theory-card-icon">📈</div>
        <h3 class="theory-card-title"><a href="/theory/dashboard/">대시보드 생성</a></h3>
        <p class="theory-card-desc">Streamlit, Dash, Plotly 등 데이터 시각화 대시보드</p>
      </div>
      <div class="theory-card">
        <div class="theory-card-icon">🧠</div>
        <h3 class="theory-card-title"><a href="/theory/ml-dl/">머신러닝/딥러닝</a></h3>
        <p class="theory-card-desc">ML 알고리즘, 딥러닝, PyTorch, TensorFlow 활용</p>
      </div>
      <div class="theory-card">
        <div class="theory-card-icon">🗄️</div>
        <h3 class="theory-card-title"><a href="/theory/data/">데이터</a></h3>
        <p class="theory-card-desc">데이터베이스, SQL, 데이터 엔지니어링 기초</p>
      </div>
      <div class="theory-card">
        <div class="theory-card-icon">⚙️</div>
        <h3 class="theory-card-title"><a href="/theory/software-engineering/">소프트웨어엔지니어링</a></h3>
        <p class="theory-card-desc">설계 패턴, 클린코드, Git, DevOps 등 SW 공학</p>
      </div>
    </div>
  </section>

</div>
