---
layout: page
title: Blog
description: List of all Blog Posts
permalink: /archive/
---


<section style="padding-top:40px;">
{% for post in site.posts %}
<div class="row">
<div class="col-lg-8 col-md-8 col-lg-offset-2 col-md-offset-2 blogposts">
  <p class="post-title-side">
    <a  href="{{ post.url | prepend: site.baseurl }}" style="color:black">{{ post.title }}</a>
  </p>
    <p class="blog-page-content">{{ post.content | strip_html | truncatewords: 50 }}</p>
  <section class="post-meta">
    <div class="post-date">{{ post.date | date: "%B %-d, %Y" }}</div>
    <div class="post-categories">
    {% if post.categories.size > 0 %}in {% for cat in post.categories %}
      {% if site.jekyll-archives %}
      <a href="{{ site.baseurl }}/category/{{ cat }}">{{ cat | capitalize }}</a>{% if forloop.last == false %}, {% endif %}
      {% else %}
      <a href="{{ site.baseurl }}/posts/#{{ cat }}">{{ cat | capitalize }}</a>{% if forloop.last == false %}, {% endif %}
      {% endif %}
    {% endfor %}{% endif %}
    </div>
  </section>
  </div>
  </div>
  <div class="row">
  <div class="col-lg-8 col-md-8 col-lg-offset-2 col-md-offset-2 blogposts-tags">
    <h4>Tags</h4>
    {% assign tags = post.tags %}
    {% for tag in tags %}
      <button class="button">{{ tag }}</button>
    {% endfor %}
    <hr>
  </div>
</div>
{% if forloop.last == false %}
{% endif %}
{% endfor %}
</section>




