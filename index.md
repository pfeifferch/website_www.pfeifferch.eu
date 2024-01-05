---
layout: page
title: Links
---
<div class="main">
  {% for post in site.posts %}
<hr>
  <a href="{{ post.excerpt | remove: '<p>' | remove: '</p>' }}" class="button" target="_blank">{{ post.title }}</a>

  {% endfor %}
</div>
