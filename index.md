---
layout: page
title: pfeifferCh's Social Media Links
---
<div class="main">
    {% for post in site.posts %}
    {% if page.iscategorylink  or post.iscategorylink  or iscategorylink %}
  <a href="?{{ post.title }}" class="button" target="_self" style="background-color: #{{ post.categorylinkbgcolor | default: "637d96" }} !important;"><img height:"auto;" width:"auto" src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b4/NotoSans_-_Open_Folder_-_1F5C1.svg/320px-NotoSans_-_Open_Folder_-_1F5C1.svg.png"> {{ post.title }}</a>
    {% else %}
  <a href="{{ post.excerpt | remove: '<p>' | remove: '</p>' }}" class="button" target="_blank">{{ post.title }}</a>
    {% endif %}
  {% endfor %}
</div>
