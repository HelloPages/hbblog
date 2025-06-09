---
layout: page
title: Microblog
permalink: /microblog/
---

<div class="microblog">
  {% assign microblog_by_year = site.categories.microblog | group_by_exp: "post", "post.date | date: '%Y'" | sort: "name" | reverse %}
  
  {% for year_group in microblog_by_year %}
  <div class="microblog-year">
    <h2>{{ year_group.name }}</h2>
    
    {% include post-list-title-only.html posts=year_group.items %}
  </div>
  {% endfor %}
  
  {% if paginator.total_pages > 1 %}
    {% include pagination.html %}
  {% endif %}
</div>
