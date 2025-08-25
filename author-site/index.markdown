---
layout: default
title: Home
---

<section class="hero">
  <img src="/assets/images/author.jpg" alt="Arati Chattopadhyay" class="author-photo">
  <h1>Arati Chattopadhyay</h1>
  <p class="tagline">Author • Storyteller • Keeper of Memories</p>
</section>

<section class="featured-works">
  <h2>Featured Works</h2>
  <ul>
    {% for work in site.works limit:3 %}
      <li>
        <a href="{{ work.url | relative_url }}">{{ work.title }}</a> – {{ work.description }}
      </li>
    {% endfor %}
  </ul>
</section>

<section class="latest-posts">
  <h2>Latest Writings</h2>
  <ul>
    {% for post in site.posts limit:3 %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a> 
        <span class="date">{{ post.date | date: "%B %d, %Y" }}</span>
      </li>
    {% endfor %}
  </ul>
</section>
