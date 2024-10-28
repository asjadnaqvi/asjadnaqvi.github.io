---
layout: page
title: stata
permalink: /projects/
description:
nav: true
nav_order: 5
display_categories: 
horizontal: false
---

I have been using **Stata** for about 20 years, but it was not until the COVID-19 lockdowns in 2020, that I started writing guides on how to do better visualizations. In Fall 2020, I created the [Stata Guide on Medium](https://medium.com/the-stata-guide) to document the processes of programming different types of visualizations. The aim of these guides was to primarily support my own work for tracking the spread of the Corona virus (since there was a lot of good data coming out back then). The writings also helped me organize and consolidate the code snippets that had started to accumulate all over the place. Even though, the popularity of these guides exploded on social media, a recurring feedback was that setting up hundreds of lines of code for one visualization was not everyone's cup of tea. Users wanted pre-canned commands which they could simply feed their data and have a few customization options. This made sense from an average Stata-user perspective, who is more focused on analysis, and fancy visualizations are an extra embellishment not really required in the research world.

In early 2021, I started converting the guides into Stata packages. As of updating this page, I have published 22 data visualization packages since then (see below). Coding these up was an intensive process, given that I was completely new to this game. Although programming took me away from writing the guides, the learning experience of coding in Stata and Mata, and the resulting engagements with organizations, academics, researchers, policy experts, and the broad community in general, was highly rewarding. Even now, I recieve several query emails every week. 

Releasing packages into the public domain is like publishing a paper, with one key difference: once a paper is published, it stays online as it is. In contrast, packages undergo continuous ex-post *peer review*, and are subjected to rigorous testing, as users (including myself) find bugs and/or request new features. Some features, such as support for weights, and label wrapping, have also been added across the board. And with 20+ packages, this is a significant time sink if you also take into account updating help files, the GitHub pages, writing release notes, checking and adding sample figures, and so on. At this point in time, most packages are looking pretty solid. The most popular ones are fairly robust, offer a wide range of features, and cater to a diverse set of user requirements. Some of the visualizations generated from these packages have also started appearing in blogs and articles (although packages citations are still missing. Hint hint!). I also now have a good sense of which packages are used more than the others.

I do plan to return to The Stata Guide eventually, with the aim of writing more about the new wisdom accumulated in the last couple of years. Even in the current state, the [Stata Guide on Medium](https://medium.com/the-stata-guide) already has over 60 articles, where some of them can be useful for those just starting out with Stata. Most of articles are also no longer paywalled. But certainly more can be written. I have also set up the [Stata Gallery on Medium](https://medium.com/the-stata-gallery) where the community continues to contribute their own amazing guides. So please also check it out and submit your own articles if you have something in mind.

## Workshops and presentations
I also regularly present at Stata conferences especially my **Advanced Visualizations with Stata** series, where I introduce new material and packages. There are currently six presentations (in addition to others) that can be [viewed here](https://github.com/asjadnaqvi/The-Stata-Guide/tree/master/presentations).

I also regularly conduct workshops and seminars. Some of these are in the public domain, e.g. my **Advanced Maps in Stata courses** (comes in three versions: 1 hour, 3 hours, or 6 hours) are offered in collaboration with [Stata UK](https://www.stata-uk.com/) every year. On the private side, I have done several workshops on topics ranging from workflow management, working with frames, visualizing hierarchical data, and making maps in Stata. Currently, I am doing about one presentation per month or so. These are usually one hour and are usually part of some regular seminar series at the host institution. If you would also like to organize one, then please reach out by email. 

## Client engagement
I work directly with clients including multilateral organizations, multilateral donors, ministries, and universities to help them set up data workflows and piplines for complex data visualizations, including fully customized outputs based on the client's corporate identity. I had not initially planned to go down this route but significant demand has emerged in the last two years and the projects are too exciting to pass. The outputs of some these projects will eventually show up in the public domain. Even though I cannot say much about them, it is usually around these projects that the packages get a flurry of upgrades. This is also when you are very likely to see a burst of activity on my social media accounts. I you also want support, then please reach out by email.

## Portfolio and packages
You can find my Stata Visualizations or **StataViz Portfolio** [website here](https://asjadnaqvi.github.io/stata-portfolio).

The list of Stata packages that are currently online are listed below (each links to an external GitHub package repository):

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