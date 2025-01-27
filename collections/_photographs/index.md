---
title: Photographs
permalink: "/photographs/"
layout: "page"
---

{% assign photographs = site.photographs | where_exp: "photograph", "photograph.url != '/photographs/'" %}
<ul>
{% for photograph in photographs %}
  <li>
    <a href="{{ photograph.url }}?{{ photograph.name }}">{{ photograph.name }}</a>
  </li>
{% endfor %}
</ul>
