---
title: Τεύχη περιοδικών
permalink: "/magazine-issues/"
layout: "page"
---

{% assign magazine-issues = site.magazine-issues | where_exp: "magazine", "magazine.url != '/magazine-issues/'" %}
<ul>
{% for magazine-issue in magazine-issues %}
  <li>
    <a href="{{ magazine-issue.url }}?{{ magazine-issue.issue_number }}">{{ magazine-issue.issue_number }}</a>
  </li>
{% endfor %}
</ul>
