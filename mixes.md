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
            <p class="fs-2 mix-title"><b>{{ page.title }}</b></p>
            <div class="tag-container">
              {% for tag in page.tags %}
                <span class="tag fs-1">{{ tag }}</span>
              {% endfor %}
            </div>
            <p class="fs-1 mix-description">{{ page.description | strip_html | truncatewords: 15 }}</p>
          </div>
        </div>
      </a>
    {% endif %}
  {% endfor %}
</div>
