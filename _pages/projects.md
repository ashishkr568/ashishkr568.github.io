---
layout: single
classes: wide
title: "Projects"
permalink: /projects/
author_profile: true
---
{% include base_path %}

<p>
This space contains details of some of the projects I have worked on to keep myself updated or to automate repetitive manual tasks. All codes are available on my <a href="https://github.com/ashishkr568">GitHub</a> repository.
<p>

<div class="pgrid">
 {% for post in site.projects %}
  {% include projects-grid.html %}
{% endfor %}
</div>

