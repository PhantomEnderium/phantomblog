---
layout: default
title: Home
---

# Posts

<div class="posts">
{% for post in site.posts %}
  <a href="{{ post.url | relative_url }}">
    <div class="post-card">
      <div class="post-date">{{ post.date | date: "%B %-d, %Y" }}</div>
      <div class="post-title" style="font-size: 1.25rem; font-weight: 600;">
        {{ post.title }}
      </div>
      {% if post.excerpt %}
        <p style="color: var(--text-muted); margin-top: 8px;">
          {{ post.excerpt | strip_html | truncate: 140 }}
        </p>
      {% endif %}
    </div>
  </a>
{% endfor %}
</div>