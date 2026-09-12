---
layout: default
---

<div class="home-editorial">
  <section class="home-hero">
    <p class="home-eyebrow">Research & writing</p>
    <h1>Writing on AI, research, and intelligent systems.</h1>
    <p class="home-intro">Independent essays and research notes on artificial intelligence, multi-agent systems, scientific discovery, and the technologies shaping modern research.</p>
    <div class="home-actions">
      <a class="home-primary" href="#articles">Browse articles</a>
      <a class="home-secondary" href="{{ '/about/' | relative_url }}">About me</a>
    </div>
  </section>

  <section class="home-feature" id="latest">
    {% assign latest = site.posts | first %}
    <div class="home-feature-meta">
      <span>Latest article</span>
      <span>{{ latest.date | date: "%d %B %Y" }}</span>
    </div>
    <a class="home-feature-card" href="{{ latest.url | relative_url }}">
      <div class="home-feature-copy">
        <h2>{{ latest.title }}</h2>
        <p>{{ latest.description }}</p>
        <div class="home-read-more">Read article <span aria-hidden="true">→</span></div>
      </div>
      <div class="home-feature-visual" aria-hidden="true">
        <div class="home-orbit home-orbit-one"></div>
        <div class="home-orbit home-orbit-two"></div>
        <div class="home-orbit home-orbit-three"></div>
        <div class="home-core"></div>
      </div>
    </a>
  </section>

  <section class="home-archive" id="articles">
    <div class="home-section-heading">
      <p class="home-eyebrow">Articles</p>
      <h2>All writing</h2>
    </div>
    <div class="home-post-list">
      {% for post in site.posts %}
        {% unless post.title == "Hello World" %}
        <a class="home-post-row" href="{{ post.url | relative_url }}">
          <span class="home-post-date">{{ post.date | date: "%d %b %Y" }}</span>
          <span class="home-post-title">{{ post.title }}</span>
          <span class="home-post-arrow" aria-hidden="true">↗</span>
        </a>
        {% endunless %}
      {% endfor %}
    </div>
  </section>
</div>
