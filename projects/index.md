---
layout: default
title: Projects
---

# Projects

<ul>
  {% for project in site.projects %}
    <li>
      <a href="{{ project.url | relative_url }}">
        {{ project.title }}
      </a>
    </li>
  {% endfor %}
</ul>
