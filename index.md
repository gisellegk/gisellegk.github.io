---
title: Home
published: true
---
{% if site.projects.size > 0 %}
<ul>
  {% for project in site.projects %}
    <li>
      <a href="{{ project.url }}">
        <h4>{{ project.title }}</h4>
      </a>
  {% endfor %}
</ul>
{% endif %}