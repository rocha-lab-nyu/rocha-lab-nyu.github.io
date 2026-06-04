---
layout: page
title: research
permalink: /research/
description: Our lab's research addresses fundamental questions in environmental change biology. In particular, we study the genetic mechanisms behind how species adapt and evolve in response to changing environmental conditions, including shifts in climate, habitat, local pathogens, and resource availability.
nav: true
nav_order: 3
horizontal: false
---

<p class="rounded p-3 mb-4" style="background-color: var(--global-warning-block-bg); color: var(--global-warning-block-text); border-left: 4px solid var(--global-warning-block);">
  🚧 This part of the website is still under construction.
</p>

<!-- _pages/projects.md (research themes) -->
<div class="projects">

{% assign sorted_projects = site.projects | sort: "importance" %}

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

</div>
