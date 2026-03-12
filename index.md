---
layout: default
title: Home
description: "Personal site and engineering notes."
---

<section class="hero">
  <h1 class="hero-title">Hi, I&apos;m {{ site.author }}.</h1>
  <p class="hero-subtitle">
    Senior backend engineer learning the frontend stack, sharing notes on systems,
    reliability, and building things for the web.
  </p>

  <div class="hero-meta">
    <span class="pill accent">Backend · Infra · Architecture</span>
    <span class="pill">Writing about what I&apos;m learning in public.</span>
  </div>
</section>

<section class="posts-list">
  <h2 class="card-title">Latest posts</h2>
  {% if site.posts and site.posts.size > 0 %}
    {% for post in site.posts limit: 5 %}
      <article class="post-list-item">
        <a class="post-link" href="{{ post.url | relative_url }}">
          <h3 class="post-title">{{ post.title }}</h3>
          <p class="post-meta">
            {{ post.date | date: "%b %-d, %Y" }}
            {% if post.tags and post.tags.size > 0 %} · {{ post.tags | join: ", " }}{% endif %}
          </p>
          {% if post.excerpt %}
            <p class="card-excerpt">{{ post.excerpt | strip_html | strip_newlines }}</p>
          {% endif %}
        </a>
      </article>
    {% endfor %}
  {% else %}
    <p class="content">
      No posts yet. Create a file under <code>_posts/</code> named
      <code>YYYY-MM-DD-title.md</code> to publish your first post.
    </p>
  {% endif %}
</section>

