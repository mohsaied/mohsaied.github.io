---
layout: page
permalink: /publications/
title: Publications
description: See my <a href="https://scholar.google.com/citations?user=q4wBpWAAAAAJ">Google Scholar profile</a> for more information.
years: [2021,2020,2019,2018,2016,2015,2014,2013,2012,2011,2009]
nav: true
---

<div class="publications">

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
