---
layout: default
---

<div class="home-editorial">
  <section class="home-hero">
    <p class="home-eyebrow">Independent research notes</p>
    <h1>AI, research systems, and the ideas changing how knowledge gets made.</h1>
    <p class="home-intro">Long-form writing on artificial intelligence, multi-agent systems, mathematical research, verification, and scientific discovery.</p>
    <div class="home-actions">
      <a class="home-primary" href="#latest">Read the latest essay</a>
      <a class="home-secondary" href="{{ '/about/' | relative_url }}">About</a>
    </div>
  </section>

  <section class="home-feature" id="latest">
    {% assign latest = site.posts | first %}
    <div class="home-feature-meta">
      <span>Latest essay</span>
      <span>{{ latest.date | date: "%d %B %Y" }}</span>
    </div>
    <a class="home-feature-card" href="{{ latest.url | relative_url }}">
      <div class="home-feature-copy">
        <h2>{{ latest.title }}</h2>
        <p>{{ latest.description }}</p>
        <div class="home-read-more">Read essay <span aria-hidden="true">→</span></div>
      </div>
      <div class="home-feature-visual" aria-hidden="true">
        <div class="home-orbit home-orbit-one"></div>
        <div class="home-orbit home-orbit-two"></div>
        <div class="home-orbit home-orbit-three"></div>
        <div class="home-core"></div>
      </div>
    </a>
  </section>

  <section class="home-topics">
    <div class="home-section-heading">
      <p class="home-eyebrow">Themes</p>
      <h2>What I write about</h2>
    </div>
    <div class="home-topic-grid">
      <div class="home-topic">
        <span class="home-topic-number">01</span>
        <h3>AI research systems</h3>
        <p>How models, tools, agents, and verification systems are being assembled into new research workflows.</p>
      </div>
      <div class="home-topic">
        <span class="home-topic-number">02</span>
        <h3>Multi-agent coordination</h3>
        <p>Parallelism, specialization, communication, synthesis, and the limits of scaling research through many agents.</p>
      </div>
      <div class="home-topic">
        <span class="home-topic-number">03</span>
        <h3>Scientific discovery</h3>
        <p>What AI-assisted mathematics and formal verification reveal about reliability, attribution, and discovery.</p>
      </div>
    </div>
  </section>

  <section class="home-archive">
    <div class="home-section-heading">
      <p class="home-eyebrow">Archive</p>
      <h2>Writing</h2>
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
