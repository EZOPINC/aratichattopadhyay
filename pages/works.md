---
layout: page
title: Works
permalink: /works/
---

# Works

A showcase of published books and upcoming projects.

{% for work in site.works %}
- [{{ work.title }}]({{ work.url | relative_url }}) – {{ work.description }}
{% endfor %}
