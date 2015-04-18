---
layout: page
title: Archive
---

# Archive

{% for post in site.posts %}
  {% capture currentmonth %}{{post.date | date: "%B"}}{% endcapture %}	
  {% capture currentyear %}{{post.date | date: "%Y"}}{% endcapture %}
  {% if currentyear != year %}
    {% if currentmonth != month %}
      <h3>{{ currentmonth }}, {{ currentyear }}</h3>
      {% capture year %}{{currentyear}}{% endcapture %} 
    {% endif %}
  {% endif %}
  <li><a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}