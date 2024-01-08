---
layout: page
title: pfeifferCh's Social Media Links
---
<div class="main">
    {% for post in site.posts %}
    {% if page.iscategorylink  or post.iscategorylink  or iscategorylink %}
  <span id="{{ post.title }}"><a href="?{{ post.title }}" class="button" target="_self" style="background-color: #{{ post.categorylinkbgcolor | default: "637d96" }} !important;"><img height="12px" width="12px" src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b9/Simpleicons_Interface_folder-black-open-shape.svg/485px-Simpleicons_Interface_folder-black-open-shape.svg.png"> {{ post.title }}</a></span>
    {% else %}
  <a href="{{ post.excerpt | remove: '<p>' | remove: '</p>' }}" class="button" target="_blank">{{ post.title }}</a>
    {% endif %}
  {% endfor %}
</div>
