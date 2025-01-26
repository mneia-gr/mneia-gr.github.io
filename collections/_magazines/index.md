---
title: Magazines
permalink: "/magazines/"
layout: "page"
---

{% assign magazines = site.magazines | where_exp: "magazine", "magazine.url != '/magazines/'" %}
<ul>
{% for magazine in magazines %}
  <li>
    <a href="{{ magazine.url }}?{{ magazine.name }}">{{ magazine.name }}</a>
  </li>
{% endfor %}
</ul>
