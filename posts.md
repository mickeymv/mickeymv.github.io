---
layout: default
title: Posts
permalink: /posts/
---

<section class="content">
  <h1>All posts</h1>
  {% if site.posts and site.posts.size > 0 %}
    <ul class="posts-list">
      {% for post in site.posts %}
        <li class="post-list-item">
          <a class="post-link" href="{{ post.url | relative_url }}">
            <h2 class="post-title">{{ post.title }}</h2>
            <p class="post-meta">
              {{ post.date | date: "%b %-d, %Y" }}
              {% if post.tags and post.tags.size > 0 %} · {{ post.tags | join: ", " }}{% endif %}
            </p>
            {% if post.excerpt %}
              <p class="card-excerpt">{{ post.excerpt | strip_html | strip_newlines }}</p>
            {% endif %}
          </a>
        </li>
      {% endfor %}
    </ul>
  {% else %}
    <p>No posts yet. Once you add some under <code>_posts/</code>, they will show up here.</p>
  {% endif %}
</section>

