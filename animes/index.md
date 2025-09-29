---
layout: default
title: "Anime Reviews"
nav_order: 6
permalink: /animes/
comments: true
---

# Anime Review Page
This is a collection of my anime reviews where I share my thoughts and opinions.

<ul>
  {% for anime in site.animes %}
    <li>
      <a href="{{ anime.url | relative_url }}">{{ anime.title }}</a>
    </li>
  {% endfor %}
</ul>
