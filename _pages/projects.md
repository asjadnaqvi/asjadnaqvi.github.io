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

I have been using **Stata** for about 20 years now. But it was not until the COVID-19 lockdowns in Vienna in 2020 when I started writing guides on how to do better visualizations with the software. In the Fall of 2020, I created the [Stata Guide on Medium](https://medium.com/the-stata-guide) to describe the processes of programming different types of visualizations. The aim of these guides was to primarily support my own work for tracking the spread of the Corona virus since there was a lot of good data coming out back then. The writings also helped me organize and consolidate the code snippets that were accumulating all over the place. Even though, the popularity of these guides exploded on social media, a recurring feedback was that setting up hundreds of lines of code for one visualization was not everyone's cup of tea. Users wanted pre-canned simple commands which they could simply feed their data with some customization options. This also made sense from an average Stata-user perspective, who is more focused on analysis, and fancy visualizations are not really required in the research world.

In early 2021, I started converting the guides into Stata packages. As of updating this page, I have published 20+ data visualization packages since then (see below). Coding these up was an intensive learning process, given that I was completely new to the game. Although programming took me away from writing the guides, the learning experience of coding in Stata and Mata, and the resulting engagements with various organizations, academics, researchers, policy experts, and the broad community, was (and is) highly rewarding.

Releasing packages into the public domain is like publishing a paper, with one key difference: once a paper is published, it stays online as it is. In contrast, packages undergo continuous ex-post *peer review*, and are subjected to rigorous testing, as users (including myself) find bugs and/or request new features. Some features, such as support for weights, and label wrapping, have also been added across the board. And with 20+ packages, this is a significant time sink if you also take into account updating help files, the GitHub pages, writing release notes, checking and adding sample figures, and so on. At this point in time, most packages are looking pretty solid. The most popular ones are fairly robust, offer a wide range of features, and cater to a diverse set of user requirements. Some of the visualizations generated from these packages have also started appearing in blogs and articles (although packages citations are still missing. Hint hint!). I also now have a good sense of which packages are used more than the others.

I do plan to eventually return to The Stata Guide with the aim of writing more about the knowledge accumulated over the last couple of years. Even in the current dormant state, the [Stata Guide on Medium](https://medium.com/the-stata-guide) has over 60 articles where most of them are still useful for those just starting out. Some of the fundamental guides are also no longer paywalled. But certainly more can be written. I have also set up the [Stata Gallery on Medium](https://medium.com/the-stata-gallery) where the community continues to contribute their own amazing guides. So please also check it out and submit your own articles if you have something in mind.

## Workshops and presentations
I regularly present at Stata conferences especially my **Advanced Visualizations with Stata** series, where I introduce new material and packages. There are currently six presentations (in addition to others) that can be [viewed here](https://github.com/asjadnaqvi/The-Stata-Guide/tree/master/presentations). I also regularly conduct workshops and seminars. Some of these are publicly offered, e.g. my **Advanced Maps in Stata courses** (comes in three versions: 1 hour, 3 hours, or 6 hours) in collaboration with [Stata UK](https://www.stata-uk.com/) every year. On the private side, I have also conduct workshops on topics ranging from workflow management, Stata frames, visualizations, and making maps in Stata. Usually I do about one presentation per month usually for one hour and are usually part of some regular seminar series at host institutions. If you would also like to organize one, then please reach out! 

## Client engagement
I also work directly with clients that range from multilateral organizations, multilateral donors, ministries, and universities to help them set up data workflows and piplines for complex data visualizations, including fully customized outputs. Going down this route was not really planned but significant demand emerged in the last years and the projects were too exciting to pass. The outputs of some these projects will eventually show up in the public domain. Even though I cannot say much about them, it is usually around these projects that the packages get a flurry of upgrades and you are likely to see a burst of activity on my social media accounts. If you also want support with large projects, visualizations, then please also reach out!

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