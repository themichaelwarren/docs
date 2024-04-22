---
layout: default
title: Mixes
nav_order: 4
has_toc: false
has_children: true
image: /assets/images/michael in living room.jpg
---

## Mixes
click a thumbnail that looks good, or even use the search above and enter a random word or artist

<div class="mix-container">
  {% assign sorted_pages = site.pages | where: 'dir', '/mixes/' | sort: 'date' | reverse %}
  {% for page in sorted_pages %}
    <div class="mix-item">
      <a href="{{ page.url | relative_url }}" class="mix-link">
        <div class="mix-thumbnail">
          <img src="{{ page.image }}" alt="{{ page.title }}">
        </div>
        <div class="mix-details">
          <h3>{{ page.title }}</h3>
          <div class="tag-container">
            {% for tag in page.tags %}
              <span class="tag">{{ tag }}</span>
            {% endfor %}
          </div>
          <p>{{ page.description | strip_html | truncatewords: 15 }}</p>
        </div>
      </a>
    </div>
  {% endfor %}
</div>
