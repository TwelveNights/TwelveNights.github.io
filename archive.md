---
layout: page
title: Archive
---

<p class="archive">Here are my blog posts, organized by year.</p>

{% for post in site.posts %}
  {% capture currentyear %}{{post.date | date: "%Y"}}{% endcapture %}
  {% if currentyear != year %}
    <li>{{ currentyear }}</li>
    {% capture year %}{{currentyear}}{% endcapture %} 
  {% endif %}
    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}