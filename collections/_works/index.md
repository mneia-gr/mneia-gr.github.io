---
title: Έργα
permalink: "/works/"
layout: "page"
---

{% assign works = site.works | where_exp: "work", "work.url != '/works/'" | sort: "name" %}
<ul>
{% for work in works %}
  <li>
    <a href="{{ work.url }}?{{ work.name }}">{{ work.name }}</a> ({{ work.type | downcase }})
  </li>
{% endfor %}
</ul>
