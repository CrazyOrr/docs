---
layout: default
---
{% for project in site.projects %}
  - [{{ project.name }}]({{ project.url }})
{% endfor %}