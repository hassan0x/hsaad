---
layout: single
author_profile: true
title: Posts
header:
  overlay_image: blog-cover.png
permalink: /posts.html
---

<ul>
{% for post in site.posts %}
  {% assign currentdate = post.date | date: "%Y" %}
  {% if currentdate != date %}
    <h3>{{ currentdate }}</h3>
    {% assign date = currentdate %} 
  {% endif %}
    <a href="{{ post.url }}">{{ post.title }}</a><br><br>
{% endfor %}
</ul>
