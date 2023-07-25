---
layout: page
title: team
permalink: /team/
description: A growing team.
nav: true
nav_order: 2
display_categories: [PhD]
horizontal: false
---



<table style="border-collapse: collapse; border: none;">
  <tr>

    <td style="border: none; padding:40px; vertical-align: middle;">
      <img src="/assets/img/henry.png" alt="Alt Text" width="120" height="160" alt="Image 1" style="border-radius: 50%;">
      <p style="font-size: 14px; text-align: center;"> <a href="https://henrysenior.com/">Henry Senior</a> <br> PhD candidate, 2021 <br> GNN, Vision-Language. <br>With Greg and Luca</p>
    </td>
    
    <td style="border: none; padding:40px; vertical-align: middle;">
      <img src="/assets/img/qifan.jpeg" alt="Alt Text" width="120" height="160" alt="Image 2" style="border-radius: 50%;">
      <p style="font-size: 14px; text-align: center;"> <a href="https://fuqifan.github.io/">Qifan Fu</a> <br> PhD candidate, 2021 <br> Sign Language. <br>With Greg and Changjae</p>
    </td>
    
    <td style="border: none; padding:40px; vertical-align: middle;">
      <img src="/assets/img/christian.jpeg" alt="Alt Text" width="120" height="160" alt="Image 2" style="border-radius: 50%;">
      <p style="font-size: 14px; text-align: center;"> <a href="https://www.christiansteinmetz.com/">Christian J. Steinmetz</a> <br> PhD candidate, 2020<br>Audio and Music. <br>With Joshua</p>
    </td>

    <td style="border: none; padding:40px; vertical-align: middle;">
      <img src="/assets/img/marco.jpeg" alt="Alt Text" width="120" height="160" alt="Image 2" style="border-radius: 50%;">
      <p style="font-size: 14px; text-align: center;"> <a href="https://mcomunita.github.io/">Marco Comunita'</a> <br> PhD candidate, 2020<br>Neural Synthesis of Sound Effects. <br>With Joshua</p>
    </td>

  </tr>
  <tr>
    <td style="border: none; padding:40px">
      <img src="/assets/img/QingWang.jpg" alt="Alt Text" width="120" height="160" alt="Image 3" style="border-radius: 50%;">
      <p style="font-size: 14px; text-align: center;"> <a href="">Qing Wang</a> <br> PhD candidate, 2023<br>Multi-modal Learning.</p>
    </td>
    <td style="border: none; padding:40px">
      <img src="/assets/img/XiaohangYang.jpg" alt="Alt Text" width="120" height="160" alt="Image 4" style="border-radius: 50%;">
      <p style="font-size: 14px; text-align: center;"> <a href="">Xiaohang Yang</a> <br> PhD candidate, 2023<br>Neural Rendering, Human Body.</p>
    </td>
    <td style="border: none; padding:40px"> 
      <img src="/assets/img/YilanDong.jpg" alt="Alt Text" width="120" height="160" alt="Image 3" style="border-radius: 50%;">
      <p style="font-size: 14px; text-align: center;"> <a href="">Yilan Dong</a> <br> PhD candidate, 2023<br>Neural Rendering, Hand Pose.</p>
    </td>
    <td style="border: none; padding:40px">
      <img src="/assets/img/JiahaoYang.jpg" alt="Alt Text" width="120" height="160" alt="Image 4" style="border-radius: 50%;">
      <p style="font-size: 14px; text-align: center;"> <a href="">Jiahao Yang</a> <br> PhD candidate, 2023<br>Neural Rendering, 4D Human Head.</p>
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


MSc students:

Nan Tia, 2022/2023

Chen-Yu Lin, 2022/2023

Rongzhi Zhong, 2022/2023

Edmund Richard Lepre, 2022/2023 
