---
layout: page
title: Notes
permalink: /notes/
---

<div class="notes">
  {% assign notes_by_year = site.categories.notes | group_by_exp: "post", "post.date | date: '%Y'" | sort: "name" | reverse %}
  
  {% for year_group in notes_by_year %}
  <div class="notes-year">
    <h2>{{ year_group.name }}</h2>
    
    {% include post-list-title-only.html posts=year_group.items %}
  </div>
  {% endfor %}
  
  {% if paginator.total_pages > 1 %}
    {% include pagination.html %}
  {% endif %}
</div>
