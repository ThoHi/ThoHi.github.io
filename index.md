---
layout: home
title: Home
---

# Welcome to ThoHi's Website

This is my personal website where I share my thoughts and experiences in technology and data science.

## Recent Posts

<ul class="post-list">
  {% for post in site.posts limit:5 %}
    <li class="post-item">
      <h2 class="post-title">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h2>
      <div class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</div>
      {% if post.excerpt %}
        <p>{{ post.excerpt }}</p>
      {% endif %}
    </li>
  {% endfor %}
</ul>

## About

I'm a technology enthusiast and data scientist working on various projects involving data analysis, visualization, and software development. My work focuses on creating practical solutions to real-world problems.

[Learn more about me →](/about) 