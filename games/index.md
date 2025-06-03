---
nav_order: 5
permalink: /games/
title: Game Reviews
---

# Game Reivew Page
This is a collection of game reviews that I have written over time. Each review includes my thoughts, ratings, and sometimes screenshots or gameplay videos.

<ul>
  {% for game in site.games %}
    <li>
      <a href="{{ game.url | relative_url }}">{{ game.title }}</a>
    </li>
  {% endfor %}
</ul>
