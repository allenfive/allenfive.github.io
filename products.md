---
layout: single
title: Products
description: "Browse A5 Productivity Tools - Chrome extensions and custom development solutions. Download productivity tools for offline viewing and content management."
permalink: /products/
classes: wide
---

## A5 Products

Check out some of the publicly available productivity tools we've built ... with more products coming soon!

{% for product in site.products %}
  <div class="product-card" style="margin-bottom: 2em; padding: 1.5em; border: 1px solid #e0e0e0; border-radius: 8px;">
    <div style="display: flex; align-items: center; gap: 1em; margin-bottom: 0.5em;">
      {% if product.url contains 'a5-skool-video-download-tool' %}
        <img src="/assets/images/skool-downloader-icon-128.png" alt="{{ product.title }} Icon" style="width: 48px; height: 48px; flex-shrink: 0;">
      {% endif %}
      <h2 style="margin: 0;"><a href="{{ product.url }}">{{ product.title }}</a></h2>
    </div>
    {% if product.header.teaser %}
      <img src="{{ product.header.teaser }}" alt="{{ product.title }} - {{ product.excerpt | strip_html | truncate: 100 }}" style="max-width: 100%; height: auto; margin: 1em 0; border-radius: 4px;">
    {% endif %}
    <p>{{ product.excerpt }}</p>
    <p><a href="{{ product.url }}" class="btn btn--primary">Learn More</a></p>
  </div>
{% endfor %}
