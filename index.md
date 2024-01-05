---
layout: page
title: Links
---
<div class="main">
{% if post.category == true %}
  {% for post in site.posts %}
  <a href="#{{ post.title }}" class="button" style="background-color: coral;">{{ post.title }}</a>
{% else %}
  {% for post in site.posts %}
  <a href="{{ post.excerpt | remove: '<p>' | remove: '</p>' }}" class="button" target="_blank">{{ post.title }}</a>
  {% endfor %}
{% endif %}
</div>
