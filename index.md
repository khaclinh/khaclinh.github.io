---
layout: default
title: Updates
nav: updates
---

<div class="hero">
  <h1>Recent updates</h1>
  <p>Short research notes, releases, milestones, travel/talks, and anything you want to timestamp.</p>
</div>

<div class="grid">
  <section class="card">
    <h2>Latest</h2>
    <ul class="list">
      {% assign items = site.updates | sort: 'date' | reverse %}
      {% for u in items limit: 10 %}
        <li class="item">
          <div class="meta">{{ u.date | date: "%Y-%m-%d" }}</div>
          <div class="title"><a href="{{ u.url | relative_url }}">{{ u.title }}</a></div>
          {% if u.excerpt %}
            <div class="excerpt">{{ u.excerpt | strip_html | truncate: 160 }}</div>
          {% endif %}
        </li>
      {% endfor %}
    </ul>

    <p style="margin-top:10px; color:var(--muted);">
      Tip: add new updates by creating Markdown files under <code>_updates/</code>.
    </p>
  </section>

  <aside class="card">
    <h2>Quick links</h2>
    <ul class="list">
      <li class="item"><div class="title"><a href="{{ '/publications/' | relative_url }}">Publications</a></div><div class="meta">Selected + full list (YAML-driven)</div></li>
      <li class="item"><div class="title"><a href="{{ '/about/' | relative_url }}">About</a></div><div class="meta">Bio, research interests, affiliations</div></li>
      <li class="item"><div class="title"><a href="{{ '/stories/' | relative_url }}">Stories</a></div><div class="meta">Longer-form writing and notes</div></li>
      <li class="item"><div class="title"><a href="{{ '/contact/' | relative_url }}">Contact</a></div><div class="meta">Email + socials</div></li>
    </ul>

    <h2 style="margin-top:14px;">Current focus</h2>
    <p style="margin:0; color:var(--muted);">
      Replace this with your current research focus (e.g., Domain Generalization for Object Detection, data augmentation, multimodal perception).
    </p>
  </aside>
</div>
