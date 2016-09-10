---
layout: page
title: Latest Posts 
excerpt: "An archive of blog posts sorted by date."
search_omit: true
image:
  feature: so-simple-sample-image-3.jpg
  credit:  deepak
  creditlink: http://research-deepak.com/home
---

<ul class="post-list">
{% for post in site.categories.blog %} 
  <li><article><a href="{{ site.url }}{{ post.url }}">{{ post.title }} <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time></span>{% if post.excerpt %} <span class="excerpt">{{ post.excerpt }}</span>{% endif %}</a></article></li>
{% endfor %}
</ul>