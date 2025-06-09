---
layout: default
title: Microblog
permalink: /microblog/
---

<div class="microblog">
  <h1 class="page-title">Microblog</h1>
  
  {% assign microblog_by_year = site.categories.microblog | group_by_exp: "post", "post.date | date: '%Y'" | sort: "name" | reverse %}
  
  {% for year_group in microblog_by_year %}
  <div class="microblog-year">
    <h2>{{ year_group.name }}</h2>
    
    {% include post-list-title-only.html posts=year_group.items %}
  </div>
  {% endfor %}
  
  {% if site.paginate %}
    {% include pagination.html %}
  {% endif %}
</div>
