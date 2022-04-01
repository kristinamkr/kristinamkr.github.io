---
layout: default
title: home
permalink: /
---

<div class="preview-wrapper">
  <nav class="link-preview">
  <ul>
  <!-- Displays 5 most recent blog posts -->
  {% for post in site.posts limit: 5 %}
  <!-- Discern post type -->
    {% if post.cover %} 
      <br>
      <div class="preview-image-card">
        <h3>
          <li><a href="{{ post.url }}">{{ post.title }}</a></li>
        </h3>
        <div class="preview-image">
      <a href="{{ post.url }}"><img src="{{ post.cover }}" alt="{{ post.alt-text }}" class="image-post-cover-preview"></a>
        </div>
        <p> {{ post.preview }} </p>
      </div>
    {% endif %} 
    {% unless post.cover %}
      <div class="preview-card">
        <h3>
          <li><a href="{{ post.url }}">{{ post.title }}</a></li>
        </h3>
        <p> {{ post.preview }} </p>
      </div>
    {% endunless %} 
  {% endfor %}
  </ul>
  </nav>
</div>
