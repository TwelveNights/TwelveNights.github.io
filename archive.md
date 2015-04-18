---
layout: page
title: Archive
---

{% for post in site.posts %}
  {% capture currentmonth %}{{post.date | date: "%B"}}{% endcapture %}	
  {% capture currentyear %}{{post.date | date: "%Y"}}{% endcapture %}
  {% if currentyear != year %}
    {% if currentmonth != month %}
      <li>{{ currentmonth }} {{ currentyear }}</li>
      {% capture year %}{{ currentyear }}{% endcapture %}
      {% capture month %}{{ currentmonth }}{% endcapture %}
    {% endif %}
  {% endif %}
  <li><a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}