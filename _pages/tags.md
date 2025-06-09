---
layout: page
title: Tags
permalink: /tags/
---

<div class="tags-page">
  {% assign tags = site.tags | sort %}
  
  <div class="tag-cloud">
    {% for tag in tags %}
      <a href="#{{ tag[0] | slugify }}" class="tag tag-{{ forloop.index | modulo: 8 }}">
        {{ tag[0] }} <span class="tag-count">({{ tag[1].size }})</span>
      </a>
    {% endfor %}
  </div>
  
  <div class="tag-list">
    {% for tag in tags %}
    <div class="tag-section" id="{{ tag[0] | slugify }}">
      <h2>{{ tag[0] }}</h2>
      <ul class="post-list">
        {% for post in tag[1] %}
        <li class="post-item">
          <span class="post-date">{{ post.date | date: "%Y-%m-%d" }}</span>
          <a href="{{ post.url | relative_url }}" class="post-link">{{ post.title }}</a>
        </li>
        {% endfor %}
      </ul>
    </div>
    {% endfor %}
  </div>
</div>
\`\`\`

最后，让我们添加一些基本的样式：
