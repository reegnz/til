---
permalink: /archive
layout: page
title: Archive
---
<ul>
  {% for post in site.posts %}
    <li>
      <a href=".{{ post.url }}">{{ post.date }} - {{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
