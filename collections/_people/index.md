---
title: People
permalink: "/people/"
layout: "page"
---

{% assign people = site.people | where_exp: "people", "people.url != '/people/'" %}
<ul>
{% for person in people %}
  <li>
    <a href="{{ person.url }}?{{ person.name }}">{{ person.name }}</a>
  </li>
{% endfor %}
</ul>
