---
layout: page
title: Projects
permalink: /projects/
nav: true
nav_order: 3
display_categories:
  - published
  - research
category_labels:
  published: Published papers
  research: Other projects
horizontal: true
---

<!-- pages/projects.md -->
<div class="projects">
{% if page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <h2 class="category font-weight-bold" id="{{ category }}">
    <a href=".#{{ category }}">{{ page.category_labels[category] | default: category }}</a>
  </h2>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1">
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
    <div class="row row-cols-1">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
