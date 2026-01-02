---
layout: single
title: A5 Productivity Tools
permalink: /
classes: wide
header:
  overlay_color: "#2563eb"
  overlay_filter: "0.3"
  actions:
    - label: "View Products"
      url: /products/
    - label: "Contact Sales"
      url: mailto:sales@allenfive.com
---

## Build Better Productivity Tools

A5 builds and sells productivity tools.

We also offer custom development services for anything from Chrome extensions, to fully built out sites, to LLM or Machine learning solutions.  Many of the solutions that we've developed are not shared here due to privacy concerns.  Contact us to discuss your project needs!

---

## Current Products

{% for product in site.products limit:3 %}
  <div style="margin-bottom: 2em; padding: 1.5em; background: #f8f9fa; border-radius: 8px;">
    <h2><a href="{{ product.url }}">{{ product.title }}</a></h2>
    {% if product.header.teaser %}
      <img src="{{ product.header.teaser }}" alt="{{ product.title }}" style="max-width: 100%; height: auto; margin: 1em 0; border-radius: 4px;">
    {% endif %}
    <p>{{ product.excerpt }}</p>
    <p><a href="{{ product.url }}" class="btn btn--primary">Learn More</a></p>
  </div>
{% endfor %}

---

## Custom Development

Need a custom Chrome extension?  Or specialty productivity tool? Or a game?  Web or Mobile, Enterprise or Startup ... we can help!

**Contact us**: [sales@allenfive.com](mailto:sales@allenfive.com)
