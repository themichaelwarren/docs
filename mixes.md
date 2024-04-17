---
layout: default
title: Mixes
nav_order: 4
has_children: true
---

## Mixes

<div class="card-container">
  {% for page in site.pages %}
    {% if page.dir == "/mixes/" %}
      <a href="{{ page.url | relative_url }}" class="card-link">
        <div class="card">
          <img src="{{ page.image }}" alt="{{ page.title }}">
          <div class="card-content">
            <p><b>{{ page.title }}</b></p>
            <p>{{ page.caption | strip_html | truncatewords: 20 }}</p>
          </div>
        </div>
      </a>
    {% endif %}
  {% endfor %}
</div>