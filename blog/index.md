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

**2016:** 
{: .notice}

[1.] Pal, D.; Vain, J . *Tester Partitioning and Synchronization Algorithm For
Testing Real-Time Distributed Systems*, 10th Junior Researcher Workshop on Real-Time Computing, Brest, France (Forthcoming). 



<ul class="post-list">
{% for post in site.categories.blog %} 
  <li><article><a href="{{ site.url }}{{ post.url }}">{{ post.title }} <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time></span>{% if post.excerpt %} <span class="excerpt">{{ post.excerpt }}</span>{% endif %}</a></article></li>
{% endfor %}
</ul>
