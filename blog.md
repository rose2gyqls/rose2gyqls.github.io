---
layout: homepage
title: Blog
permalink: /blog.html
---

## Blog

<div class="blog-list">
{% for post in site.posts %}
<div class="blog-item">
  <span class="blog-date">{{ post.date | date: "%Y.%m.%d" }}</span>
  <h3 class="blog-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
  {% if post.description %}
  <p class="blog-description">{{ post.description }}</p>
  {% endif %}
  {% if post.tags.size > 0 %}
  <div class="blog-tags">
    {% for tag in post.tags %}
    <span class="blog-tag">{{ tag }}</span>
    {% endfor %}
  </div>
  {% endif %}
</div>
{% endfor %}
</div>

{% if site.posts.size == 0 %}
<p>No posts yet.</p>
{% endif %}
