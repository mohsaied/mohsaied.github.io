---
layout: page
title: Team
permalink: /team/
description:
nav: true
display_categories: [current, past]
horizontal: false
---
<div class="projects">
  {% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
    {% for category in page.display_categories %}
      <h2 class="category">{{category}}</h2>
      {% assign categorized_projects = site.team | where: "category", category %}
      {% assign sorted_projects = categorized_projects | sort: "importance" %}
      <!-- Generate cards for each project -->
      <div class="grid">
        {% for project in sorted_projects %}
          {% include people.html %}
        {% endfor %}
      </div>
    {% endfor %}

  {% else %}
  <!-- Display projects without categories -->
    {% assign sorted_projects = site.team | sort: "importance" %}
    <!-- Generate cards for each project -->
    <div class="grid">
      {% for project in sorted_projects %}
        {% include people.html %}
      {% endfor %}
    </div>
  {% endif %}

</div>
