---
layout: page
title: Teaching
permalink: /teaching/
description:
nav: true
display_categories: 
horizontal: false
---

<div class="projects">
  {% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
    {% for category in page.display_categories %}
      <h2 class="category">{{category}}</h2>
      {% assign categorized_projects = site.courses | where: "category", category %}
      {% assign sorted_projects = categorized_projects | sort: "importance" %}
      <!-- Generate cards for each project -->
      <div class="grid">
        {% for project in sorted_projects %}
          {% include courses.html %}
        {% endfor %}
      </div>
    {% endfor %}

  {% else %}
  <!-- Display projects without categories -->
    {% assign sorted_projects = site.courses | sort: "importance" %}
    <!-- Generate cards for each project -->
    <div class="grid">
      {% for project in sorted_projects %}
        {% include courses.html %}
      {% endfor %}
    </div>
  {% endif %}

</div>

<div>
<br><br><br><br><br><br>
</div>
