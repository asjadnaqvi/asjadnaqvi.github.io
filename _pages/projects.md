---
layout: page
title: Stata
permalink: /projects/
description:
nav: true
nav_order: 5
display_categories: 
horizontal: false
---

I have been using Stata for about 20 years but it was not till the 2020 COVID-19 lockdowns that I started writing guides on how to do better visualizations in Stata. This led me to create the [Stata Guide on Medium](https://medium.com/the-stata-guide) in the Fall of 2020. The aim of this publication was primarily to support my own work for creating visualizations in Stata in order to track the spread of the Corona virus. Writing these guides also helped me organize and consolidate the code snippets that tend to start accumulating in different folders. Even though, the popularity of these guides exploded on social media, a recurring feedback was that setting up hundreds of line of code for one visualization was not feasible. People wanted pre-canned commands to simple feed in their data customization options. This makes sense also from an average Stata-user perspective, which is more focused on analysis.

Therefore, in early 2021, I started converting the guides in Stata packages. As of updating this page, I have 23 published packages (see below). Even though, this took me away from writing guides, just the learning experience of coding in Stata and Mata, and the engagements it created with organizations, professors, and power users from across the globe was worth it. Even now, I recieve a few emails per week. 

Putting out packages in the public domain is like publishing a paper. The main difference is that once a paper is published, it stays online as it is. In contrast, packages are ""peer reviewed" ex-post, and are subjected to brutal testing, bugs and errors are found, and features are requested. Packages also get across the board updates such as support for weights, and label wrapping. This is quite a lot of work with 20+ packages and a significant time sink as well. This means long nights and work on weekends. But currently, most packages are at a solid point, and have also started appearing in blogs and articles as well. So I do plan to return to The Stata Guide soon where currently I have over 60 published articles, most of which are no longer paywalled. I have also set up the [Stata Gallery on Medium](https://medium.com/the-stata-gallery) where the community continues to contribute their amazing guides. So please also check it out and contribute your own articles as well if you have something in mind.

I also regularly present at Stata conferences especially my "Advanced Visualizations with Stata" series, where I usually introduce new material. There are currently six presentations that can be [viewed here](https://github.com/asjadnaqvi/The-Stata-Guide/tree/master/presentations).

I also regularly conduct workshops and seminars. These could be in the public domain, e.g. my Advanced Maps in Stata course (comes in three versions: 1 hour, 3 hours, and 6 hours) are offered in collaboration with [Stata UK](https://www.stata-uk.com/) every year. On the private side, I get invites to present different topics that have ranged from Stata workflows, working with frames, visualizing hierarchical data, and maps in Stata. Currently, I do about one presentation (mostly online) per month and it is usually for one hour. If you would also like to organize one, then please reach out by email! 

In addition to this, I also work directly with clients including MDBs, ministries, universities to help them set up data workflows and data visualization infrastructure in Stata. The outputs of some these will be eventually available in the public domain. But it is usually around these projects, where packages get a set of upgrades and you are more likely to see a burst of activity on social media from my end. If you have complex projects that need support, then please also reach out! 


You can find my Stata Visualizations or [StataViz portfolio here](https://asjadnaqvi.github.io/stata-portfolio/tags/portfolio/) and the list of online Stata packages below:

<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>