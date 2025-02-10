---
title: Publishers
permalink: "/publishers/"
layout: "page"
---

{% assign publishers = site.publishers | where_exp: "publisher", "publisher.url != '/publishers/'" %}
<ul>
{% for publisher in publishers %}
  <li>
    <a href="{{ publisher.url }}?{{ publisher.name }}">{{ publisher.name }}</a>
  </li>
{% endfor %}
</ul>
