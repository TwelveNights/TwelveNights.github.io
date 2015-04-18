---
layout: page
title: Archive
---

<p class="archive">Here are my blog posts, organized by date.</p>

{% for post in site.posts %}
  *{{ post.date | date_to_string }}<br />&raquo;[ {{ post.title }} ]({{ post.url }})
{% endfor %}