---
layout: default
title: Publications
nav: publications
permalink: /publications/
---

<div class="hero">
  <h1>Publications</h1>
  <p>A lightweight, editable publications list (stored in <code>_data/publications.yml</code>).</p>
</div>

<div class="card">
  <h2>Selected</h2>
  <ul class="list">
    {% assign pubs = site.data.publications | sort: 'year' | reverse %}
    {% for p in pubs %}
      {% if p.selected %}
      <li class="item">
        <div class="title">{{ p.title }}</div>
        <div class="meta">
          {{ p.authors }} · <strong>{{ p.venue }}</strong> ({{ p.year }})
          {% if p.links %}
            ·
            {% for l in p.links %}
              <a href="{{ l.url }}">{{ l.label }}</a>{% unless forloop.last %} · {% endunless %}
            {% endfor %}
          {% endif %}
        </div>
      </li>
      {% endif %}
    {% endfor %}
  </ul>
</div>

<div class="card" style="margin-top:14px;">
  <h2>All publications</h2>
  <ul class="list">
    {% assign pubs = site.data.publications | sort: 'year' | reverse %}
    {% for p in pubs %}
      <li class="item">
        <div class="title">{{ p.title }}</div>
        <div class="meta">
          {{ p.authors }} · <strong>{{ p.venue }}</strong> ({{ p.year }})
          {% if p.links %}
            ·
            {% for l in p.links %}
              <a href="{{ l.url }}">{{ l.label }}</a>{% unless forloop.last %} · {% endunless %}
            {% endfor %}
          {% endif %}
        </div>
      </li>
    {% endfor %}
  </ul>

  <p style="color:var(--muted); margin-top:10px;">
    Tip: you can also link to Google Scholar and keep this page as “selected only”.
  </p>
</div>
