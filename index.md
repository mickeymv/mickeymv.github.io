---
layout: default
title: Home
description: "Personal site and engineering notes."
---

<section class="hero">
  <div class="hero-layout">
    <div class="hero-text">
      <h1 class="hero-title">Hi, I&apos;m {{ site.author }}.</h1>
      <p class="hero-subtitle">
        Senior backend engineer learning the frontend stack, sharing notes on systems,
        reliability, and building things for the web.
      </p>

      <div class="hero-meta">
        <span class="pill accent">Backend · Infra · Architecture</span>
        <span class="pill">Writing about what I&apos;m learning in public.</span>
      </div>
    </div>

    <div class="hero-photo">
      <img
        src="{{ '/assets/img/mickey-photo.jpeg' | relative_url }}"
        alt="Photo of {{ site.author }}"
      />
    </div>
  </div>
</section>

