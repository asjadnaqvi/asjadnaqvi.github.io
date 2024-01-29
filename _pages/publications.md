---
layout: page
permalink: /publications/
title: publications
years: [2024, 2023, 2022, 2021, 2020, 2019, 2018, 2017, 2015, 2014]
nav: true
nav_order: 3
---

This page only shows papers in the public domain. For working papers, reports, or project-related documents, please reach out.

<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
