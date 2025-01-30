---
title: Works
permalink: "/works/"
layout: "page"
---

{% assign works = site.works | where_exp: "work", "work.url != '/works/'" %}
<ul>
{% for work in works %}
  <li>
    <a href="{{ work.url }}?{{ work.name }}">{{ work.name }}</a>
  </li>
{% endfor %}
</ul>
