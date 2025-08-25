---
layout: page
title: Blog
permalink: /blog/
---

# Articles & Reflections

{% for post in paginator.posts %}
- [{{ post.title }}]({{ post.url | relative_url }})  
  *{{ post.date | date: "%B %d, %Y" }}*
{% endfor %}

<div class="pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path | relative_url }}">← Newer Posts</a>
  {% endif %}

  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path | relative_url }}">Older Posts →</a>
  {% endif %}
</div>
