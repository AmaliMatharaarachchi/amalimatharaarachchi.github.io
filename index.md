---
layout: default
---

<div class="home-journal">
  <section class="home-note-hero">
    <p class="home-note-label">A quiet corner of the internet</p>
    <blockquote class="home-note-quote">
      <p>“I write to find out what I think.”</p>
      <cite>— Joan Didion</cite>
    </blockquote>
    <p class="home-note-intro">Sparse notes, quiet observations, and things jotted down along the way.</p>
    <div class="home-note-links">
      <a href="#articles">Browse notes</a>
      <a href="{{ '/about/' | relative_url }}">About me</a>
    </div>
  </section>

  {% assign latest = site.posts | first %}
  <section class="home-latest-note">
    <div class="home-note-section-head">
      <span>Latest</span>
      <span>{{ latest.date | date: "%d %B %Y" }}</span>
    </div>
    <a class="home-latest-link" href="{{ latest.url | relative_url }}">
      <div class="home-latest-text">
        <h2>{{ latest.title }}</h2>
        {% if latest.description %}<p>{{ latest.description }}</p>{% endif %}
        <span class="home-text-link">Read note →</span>
      </div>
      <div class="home-latest-image">
        <img src="{{ '/assets/images/article1/figure-1-vortex.png' | relative_url }}" alt="Illustration accompanying the latest article" loading="eager">
      </div>
    </a>
  </section>

  <section class="home-notes-index" id="articles">
    <div class="home-note-section-head home-note-section-title">
      <span>Notes</span>
      <span>Archive</span>
    </div>
    <div class="home-note-list">
      {% for post in site.posts %}
        {% unless post.title == "Hello World" %}
        <a class="home-note-row" href="{{ post.url | relative_url }}">
          <span class="home-note-date">{{ post.date | date: "%d %b %Y" }}</span>
          <span class="home-note-title">{{ post.title }}</span>
          <span class="home-note-arrow" aria-hidden="true">↗</span>
        </a>
        {% endunless %}
      {% endfor %}
    </div>
  </section>
</div>
