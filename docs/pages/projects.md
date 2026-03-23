---
layout: single
title: "Projects"
permalink: /projects/
classes: wide
---
Here are some of the projects I've worked on recently. Click on any project to read more about it!

<div class="grid__wrapper">
  {% assign projects = site.projects | where: "project_main", true %}
  {% for post in projects %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>
