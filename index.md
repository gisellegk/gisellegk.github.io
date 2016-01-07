---
title: Home
layout: home
published: true
---
{% if site.projects.size > 0 %}
<ul>
  {% for project in site.projects %}
    <li class="project">
      <a href="{{ project.url }}">{{ project.title }}</a>
    </li>
  {% endfor %}
</ul>
{% endif %}