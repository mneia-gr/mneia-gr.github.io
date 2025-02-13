---
title: Πρόσωπα
permalink: "/people/"
layout: "page"
---

{% assign people = site.people | where_exp: "person", "person.url != '/people/'" | sort: "name" %}
<ul>
{% for person in people %}
  <li>
    <a href="{{ person.url }}?{{ person.name }}">{{ person.name }}</a>
  </li>
{% endfor %}
</ul>
