---
layout: default
title: "Book Reviews"
nav_order: 3
permalink: /books/
comments: true
---

# Book Reivew Page
This is a collection of my book reviews. I hope you find them helpful in choosing your next read and share your thoughts on the books you read.

<ul>
  {% for book in site.books %}
    <li>
      <a href="{{ book.url | relative_url }}">{{ book.title }}</a>
    </li>
  {% endfor %}
</ul>
