---
layout: page
title: Art Projects
permalink: /art/
nav: false
horizontal: false
---

<div class="projects">
  {% assign art_projects = site.projects | where: "category", "art" %}
  {% assign sorted_projects = art_projects | sort: "importance" %}
  
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
</div>
