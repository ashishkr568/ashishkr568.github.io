---
title: "Archive"
layout: single
permalink: /archive/
author_profile: true
toc: true
toc_label: "Index"
toc_icon: "archive"  # corresponding Font Awesome icon name (without fa prefix)
toc_sticky: true
---
## Blog Posts By Year & Month

<ul class="taxonomy__index">
  {% assign postsInYear = site.posts | group_by_exp: 'post', 'post.date | date: "%Y"' %}
  {% for year in postsInYear %}
    <li>
      <a href="/archive/{{ year.name }}">
        <strong>{{ year.name }}</strong> <span class="taxonomy__count">{{ year.items | size }}</span>
      </a>
      <ul class="subtaxonomy__index">
      {% assign postsInMonth = year.items | group_by_exp: 'post', 'post.date | date: "%B %m"' %}
         {% for month in postsInMonth %}
         <li>
      <a href="/archive/{{ year.name | slugify  }}/{{ month.name | slice: -2, 2 | slugify }}">
        <strong>{{ month.name | truncatewords: 1, "" }}</strong> <span class="taxonomy__count">{{ month.items | size }}</span>
      </a>
      </li>
  {% endfor %}
      </ul>
    </li>
  {% endfor %}
</ul>

## Blog Posts By Categories 

{% assign categories_max = 0 %}
{% for category in site.categories %}
  {% if category[1].size > categories_max %}
    {% assign categories_max = category[1].size %}
  {% endif %}
{% endfor %}

<ul class="taxonomy__index">
  {% for i in (1..categories_max) reversed %}
    {% for category in site.categories %}
      {% if category[1].size == i %}
        <li>
          <a href="/archive/categories/{{ category[0] | slugify }}">
            <strong>{{ category[0] }}</strong> <span class="taxonomy__count">{{ i }}</span>
          </a>
        </li>
      {% endif %}
    {% endfor %}
  {% endfor %}
</ul>

## Blog Posts By Tags

<p class="tag__cloud exclude-from-search" style="text-align: center;">
  {% capture site_tags %}{% for tag in site.tags %}{{ tag | first }}{% unless forloop.last %},{% endunless %}{% endfor %}{% endcapture %}
  {% assign tags = site_tags | split:',' | sort %}
  {% include tagcloud.html %}
  </p>

<br>
{% assign tags_max = 0 %}
{% for tag in site.tags %}
  {% if tag[1].size > tags_max %}
    {% assign tags_max = tag[1].size %}
  {% endif %}
{% endfor %}

<ul class="taxonomy__index">
  {% for i in (1..tags_max) reversed %}
    {% for tag in site.tags %}
      {% if tag[1].size == i %}
        <li>
          <a href="/archive/tags/{{ tag[0] | slugify }}">
            <strong>{{ tag[0] }}</strong> <span class="taxonomy__count">{{ i }}</span>
          </a>
        </li>
      {% endif %}
    {% endfor %}
  {% endfor %}
</ul>


