---
layout: page
permalink: /publications/
title: Publications
description: Publications by categories in reversed chronological order
years_journal: [2022, 2021]
years_conf: [2022, 2021, 2020, 2019, 2017, 2016]
years_poster: [2021]
nav: true
---

<h2>Journals</h2>
<div class="publications">

{% for y in page.years_journal %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @article[year={{y}}]* %}
{% endfor %}

</div>

<h2>Conferences/Workshops</h2>
<div class="publications">

{% for y in page.years_conf %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @inproceedings[year={{y}}]* %}
{% endfor %}

</div>

<h2>Posters</h2>
<div class="publications">

{% for y in page.years_poster %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f posters -q @inproceedings[year={{y}}]* %}
{% endfor %}

</div>
