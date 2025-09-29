---
layout: default
title: "Etc"
nav_order: 7
permalink: /blog/
comments: true
---

# Etc page


<ul>
{% for post in site.posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.date | date: "%Y-%m-%d" }} — {{ post.title }}</a>
  </li>
{% endfor %}
</ul>

