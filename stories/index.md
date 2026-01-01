---
layout: default
title: Stories
nav: stories
permalink: /stories/
---

<div class="hero">
  <h1>Stories</h1>
  <p>Longer posts: project notes, travel reports, behind-the-scenes, tutorials, and reflections.</p>
</div>

<div class="card">
  <h2>Latest stories</h2>
  <ul class="list">
    {% assign items = site.stories | sort: 'date' | reverse %}
    {% for s in items limit: 20 %}
      <li class="item">
        <div class="meta">{{ s.date | date: "%Y-%m-%d" }}</div>
        <div class="title"><a href="{{ s.url | relative_url }}">{{ s.title }}</a></div>
        {% if s.excerpt %}
          <div class="excerpt">{{ s.excerpt | strip_html | truncate: 170 }}</div>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</div>
