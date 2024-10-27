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

I have been using Stata for about 20 years but it was not till the 2020 COVID-19 lockdowns that I started writing guides on how to do better visualizations. This led me to create the [**Stata Guide on Medium**](https://medium.com/the-stata-guide) in the Fall of 2020. The aim of this publication was primarily to support my own work for creating visualizations in Stata in order to track the spread of the Corona virus. Writing these guides also helped me organize and consolidate the code snippets that tend to start accumulating in different folders. Even though, the popularity of these guides exploded on social media, a recurring feedback was that setting up hundreds of line of code for one visualization was not feasible. People wanted pre-canned commands to simple feed in their data customization options. This makes sense also from an average Stata-user perspective, which is more focused on analysis.

In early 2021, I started converting the guides into Stata packages. As of updating this page, I have published 22 data visualization packages (see below). Although, this took me away from writing guides, just the learning experience of coding in Stata and Mata, and the resulting engagements with organizations, academics, policy experts, and other power users was (is) highly rewarding. Even now, I recieve several emails weekly discussing the guides and visualiztions. 

Releasing packages into the public domain is like publishing a paper, with one key difference: once a paper is published, it stays online as it is. In contrast, packages undergo continuous "peer reviewed" ex-post, and are subjected to rigorous testing, as users (and myself) find bugs and request new features. Packages sometimes also get features such as support for weights, and label wrapping across the board. With 20+ packages, this is a significant time sink and this means long nights and extra work on weekends. However, most packages are currently at a solid stage, fairly robust, with a wide range of features, catering to a very diverse audience. They have also started appearing in blogs and articles (although packages citations are still missing. Hint!).

I do plan to return to The Stata Guide eventually and start about the accumulated wisdom attained in the past couple of years. The Stata Guide on Medium already has over 60 articles most of which are no longer paywalled. I have also set up the [**Stata Gallery on Medium**](https://medium.com/the-stata-gallery) where the community continues to contribute their amazing guides. So please also check it out and contribute your own articles as well if you have something in mind.

I also regularly present at Stata conferences especially my **Advanced Visualizations with Stata** series, where I introduce new material and packges. There are currently six presentations that can be [**viewed here**](https://github.com/asjadnaqvi/The-Stata-Guide/tree/master/presentations).

I also regularly conduct workshops and seminars. Some of these are in the public domain, e.g. my **Advanced Maps in Stata course** (comes in three versions: 1 hour, 3 hours, and 6 hours) are offered in collaboration with [Stata UK](https://www.stata-uk.com/) every year. On the private side, I have done presentations on various topics ranging from Stata workflows, working with frames, visualizing hierarchical data, and maps in Stata. Currently, I do about one presentation (usually online) every month or so. These are usually one hour and are typically part of department seminar series. If you would also like to organize one, then please reach out by email! 

In addition to this, I also work directly with clients including multilateral organizations, multilateral donors, ministries, and universities to help them set up data workflows and data visualization infrastructure. The outputs of some these engagements will be eventually be made public. Even though these projects are under strict NDAs, it is usually around their activities where packages get upgrades. This is also when you are very likely to see a burst of activity on social media from my accounts. If you have projects that need support, then please also reach out for an initial discussion! 


You can find my Stata Visualizations or **StataViz portfolio** [**here**](https://asjadnaqvi.github.io/stata-portfolio/tags/portfolio/) and the list of Stata packages below (each links to an external GitHub package repository):

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