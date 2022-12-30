---
layout: page
permalink: /publications/
title: publications
description: Please visit <a href="https://scholar.google.com/citations?user=oWGGVpYAAAAJ"><b>Google Scholar</b></a> for the latest updates. Peer-reviewed publications are marked.
years: [2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014]
nav: true
nav_order: 3
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
