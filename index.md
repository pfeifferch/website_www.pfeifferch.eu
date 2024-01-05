---
layout: page
title: Links
---
<div class="main">
{% if page.iscategorylink == 'true' or post.iscategorylink == 'true' or iscategorylink == 'true' %}
  {% for post in site.posts %}
  <a href="?{{ post.title }}" class="button" target="_self" style="background-color: coral !important;">{{ post.title }}</a>
  {% endfor %}
{% else %}
  {% for post in site.posts %}
  <a href="{{ post.excerpt | remove: '<p>' | remove: '</p>' }}" class="button" target="_blank">{{ post.title }}</a>
  {% endfor %}
{% endif %}
</div>
