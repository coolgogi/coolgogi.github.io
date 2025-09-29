---
layout: default
title: "Movie Reviews"
nav_order: 4
permalink: /movies/
comments: true
---

# Movie Review Page
This is a collection of my movie reviews where I share my thoughts and opinions on various films I've watched.

<ul>
  {% for movie in site.movies %}
    <li>
      <a href="{{ movie.url | relative_url }}">{{ movie.title }}</a>
    </li>
  {% endfor %}
</ul>
