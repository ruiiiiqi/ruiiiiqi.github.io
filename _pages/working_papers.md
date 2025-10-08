---
layout: page
title: working papers
permalink: /working-papers/
nav: false
nav_order: 3
---

<div class="working-papers">
  {% assign sorted_papers = site.working_papers | sort: "year" | reverse %}

  {% for paper in sorted_papers %}
    <div class="paper">
      <h3>{{ paper.title }}</h3>
      <p class="authors"><strong>Authors:</strong> {{ paper.authors }}</p>
      <p class="abstract"><strong>Abstract:</strong> {{ paper.abstract }}</p>
      <div class="links">
        {% if paper.pdf %}
          <a href="{{ paper.pdf }}" class="btn" target="_blank">PDF</a>
        {% endif %}
        {% if paper.arxiv %}
          <a href="{{ paper.arxiv }}" class="btn" target="_blank">arXiv</a>
        {% endif %}
      </div>
      <hr>
    </div>
  {% endfor %}
</div>

