---
layout: archive
title: "Portfolio"
date: 2014-05-30T11:40:45-04:00
modified:
excerpt: "Thinking like a scientist, coding like an artist."
tags: []
image:
  feature:
  teaser:
---

<div class="tiles">
{% for post in site.categories.portfolio %}
  {% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles -->
