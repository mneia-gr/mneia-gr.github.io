---
title: Βιβλία
permalink: "/books/"
layout: "page"
---

{% assign books = site.books | where_exp: "book", "book.url != '/books/'" | sort: "name" %}
<ul>
{% for book in books %}
  <li>
    <a href="{{ book.url }}?{{ book.name }}">{{ book.name }}</a>
  </li>
{% endfor %}
</ul>
