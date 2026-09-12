---
layout: default
---

<div class="home-journal">
  <section class="home-note-hero">
    <blockquote class="home-note-quote">
      <p>“I write to find out what I think.”</p>
      <cite>— Joan Didion</cite>
    </blockquote>
    <p class="home-note-intro">Sparse notes, quiet observations, and things jotted down along the way.</p>
    <div class="home-note-links">
      <a class="home-note-primary" href="#articles">Browse notes <span aria-hidden="true">→</span></a>
      <a class="home-note-secondary" href="{{ '/about/' | relative_url }}">About me <span aria-hidden="true">→</span></a>
    </div>
  </section>

  {% assign latest = site.posts | first %}
  <section class="home-latest-note">
    <div class="home-note-section-head">
      <span>Latest</span>
    </div>
    <a class="home-latest-link" href="{{ latest.url | relative_url }}">
      <div class="home-latest-text">
        <h2>{{ latest.title }}</h2>
        {% if latest.description %}<p>{{ latest.description }}</p>{% endif %}
        <div class="home-latest-meta">{{ latest.date | date: "%b %-d, %Y" }}</div>
        <span class="home-text-link">Read more <span aria-hidden="true">→</span></span>
      </div>
      <div class="home-latest-image">
        <img src="{{ '/assets/images/article1/figure-1-vortex.png' | relative_url }}" alt="Illustration accompanying the latest article" loading="eager">
      </div>
    </a>
  </section>

  <section class="home-notes-index" id="articles">
    <div class="home-note-section-head">
      <span>All notes</span>
    </div>
    <div class="home-note-list">
      {% for post in site.posts %}
        {% unless post.title == "Hello World" %}
        <a class="home-note-row" href="{{ post.url | relative_url }}">
          <span class="home-note-date">{{ post.date | date: "%b %-d, %Y" }}</span>
          <span class="home-note-title">{{ post.title }}</span>
          <span class="home-note-arrow" aria-hidden="true">→</span>
        </a>
        {% endunless %}
      {% endfor %}
    </div>
  </section>
</div>
