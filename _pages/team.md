---
layout: page
title: team
permalink: /team/
description: A growing team.
nav: true
nav_order: 2
display_categories: [PhD, Master]
horizontal: false
---





<table style="border-collapse: collapse;">
  <tr>
    <td>
      <img src="/assets/img/henry.png" alt="Alt Text" width="160" height="250" alt="Image 1">
      <p>Henry Senior</p>
    </td>
    
    <td>
      <img src="/assets/img/qifan.jpeg" alt="Alt Text" width="160" height="250" alt="Image 2">
      <p>QIfan Fu</p>
    </td>
    
    <td>
      <img src="/assets/img/christian.jpeg" alt="Alt Text" width="160" height="250" alt="Image 2">
      <p>Christian J. Steinmetz</p>
    </td>

    <td>
      <img src="/assets/img/marco.jpeg" alt="Alt Text" width="160" height="250" alt="Image 2">
      <p>MARCO COMUNITA'</p>
    </td>

  </tr>
  <tr>
    <td>
      <img src="/assets/img/QingWang.jpg" alt="Alt Text" width="160" height="250" alt="Image 3">
      <p>Qing Wang, 2023</p>
    </td>
    <td>
      <img src="/assets/img/XiaohangYang.jpg" alt="Alt Text" width="160" height="250" alt="Image 4">
      <p>Xiaohang Yang, 2023</p>
    </td>
    <td>
      <img src="/assets/img/YilanDong.jpg" alt="Alt Text" width="160" height="250" alt="Image 3">
      <p>Yilan Dong, 2023</p>
    </td>
    <td>
      <img src="/assets/img/JiahaoYang.jpg" alt="Alt Text" width="160" height="250" alt="Image 4">
      <p>Jiahao Yang, 2023</p>
    </td>
  </tr>
</table>





<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>
