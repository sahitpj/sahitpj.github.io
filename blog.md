---
layout: page
title: Blog
description: List of all Blog Posts
permalink: /archive/
---

<div class="row row-about-page">
<div class="col-lg-8  col-lg-offset-2 col-md-8 col-md-offset-2 col-sm-8  col-sm-offset-2 archive-page">
<h1 class="archive-title">{{ page.title }}</h1>

<ul class="blog-list-items">
  {% for post in site.posts %}
    {% unless post.next %}
      <h3 class="blog-year">{{ post.date | date: '%Y' }}</h3>
    {% else %}
      {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
      {% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
      {% if year != nyear %}
        <br>
        <h3>{{ post.date | date: '%Y' }}</h3>
      {% endif %}
    {% endunless %}
    <time>{{ post.date | date:"%d %b" }}</time>&nbsp;&nbsp;&nbsp;<a href="{{ post.url }}">{{ post.title }}</a><br>
  {% endfor %}
</ul>



<br><br><br>
</div>
</div>