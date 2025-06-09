---
layout: default
title: Posts
permalink: /posts/
---

<div class="posts">
  <h1 class="page-title">Posts</h1>
  
  {% assign posts_by_year = site.categories.posts | group_by_exp: "post", "post.date | date: '%Y'" | sort: "name" | reverse %}
  
  {% for year_group in posts_by_year %}
  <div class="posts-year">
    <h2>{{ year_group.name }}</h2>
    
    {% include post-list-title-only.html posts=year_group.items %}
  </div>
  {% endfor %}
  
  {% if site.paginate %}
    {% include pagination.html %}
  {% endif %}
</div>
