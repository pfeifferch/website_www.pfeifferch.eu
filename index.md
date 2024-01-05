---
layout: page
title: pfeifferCh's Social Media Links
---
<div class="main">
  {{ page.iscategorylink }}
  {{ post.iscategorylink }}
  {% for post in site.posts %}
    {% if page.iscategorylink  or post.iscategorylink  or iscategorylink %}
  <a href="?{{ post.title }}" class="button" target="_self" style="background-color: coral !important;">{{ post.title }}</a>
    {% else %}
  <a href="{{ post.excerpt | remove: '<p>' | remove: '</p>' }}" class="button" target="_blank">{{ post.title }}</a>
    {% endif %}
  {% endfor %}
</div>
