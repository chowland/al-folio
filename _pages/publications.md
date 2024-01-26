---
layout: page
permalink: /publications/
title: publications
description: Here you can find all my peer-reviewed publications, preprints, theses and other reports. If there are any documents here that you cannot access, please get in touch and I would be happy to send you a copy.
years: [2024, 2023, 2022, 2021, 2020, 2018, 2016]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

<h2 class="year">preprints</h2>
{% bibliography -f preprints %}

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

<h2 class="year">theses</h2>
{% bibliography -f theses %}

<h2 class="year">reports</h2>
{% bibliography -f reports %}

</div>
