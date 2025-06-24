---
layout: page
title: Team
permalink: /team/
redirect: https://abdelfattah-lab.github.io/
description: Click for the <a href="https://confluence.cornell.edu/display/abdelfattah">internal group wiki</a>.
nav: false
display_categories: [current, past]
horizontal: false
---
<div class="projects">
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
</div>

#### More students:
- Yifei Gao. MEng Researcher (2024)
- Yunhao Hu. MEng Researcher (2024)
- Aditya Kotha. Undergrad Researcher (2024)
- Xilai Dai. Undergrad Researcher (Summer 2023)
- Yassine Ghannane. Undergrad Researcher (Summer 2022)
