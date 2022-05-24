---
layout: page
permalink: /publications/
title: publications
nav: true
description: My publications in reverse chronological order with highlights in <strong>bold</strong>.
years: [2022, 2021, 2019]
order: 7
---

<h3 class="year">In prep.</h3>
{% bibliography -f preprints %}

{% for y in page.years %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

