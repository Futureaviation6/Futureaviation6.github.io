---
layout: default
title: Aviation 2040
description: "The future of aviation is here! Supersonic flights in 3 hours, electric & hydrogen aircraft, flying taxis, vertiports, space tourism, and the end of kerosene."
---

<div class="home-hero">
  <h1>Future Smartphones<br><span>2030–2040</span></h1>
  <p class="subtitle">Everything already funded and built</p>
</div>

<div class="posts-grid">
  {% assign sorted_posts = site.posts | reverse %}
  {% for post in sorted_posts %}
    {% assign first_image = post.content | split:'src="' | slice:1 | first | split:'"' | first %}

    <article class="post-card">
      <a href="{{ post.url }}">
        <div class="post-thumb-wrapper">
          <img src="{{ first_image }}" alt="{{ post.title }}" class="post-thumb">
        </div>
        <div class="post-info">
          <h2>{{ post.title | split: ". " | last }}</h2>
          <p class="post-desc">{{ post.description }}</p>
          <span class="read-more">Read chapter</span>
        </div>
      </a>
    </article>
  {% endfor %}
</div>

<div class="made-with">
  <p>All images • Full offline • No tracking • Built December 2025</p>
</div>
