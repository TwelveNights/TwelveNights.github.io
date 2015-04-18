---
layout: page
title: Archive
---

<p class="archive">Here are my blog posts, organized by date.</p>

{% for post in site.posts %}
    {% capture month %}{{ post.date | date: '%B %Y' }}{% endcapture %}
    {% capture next-month %}{{ post.next.date | date: '%B %Y' }}{% endcapture %}
    {% if month != next-month %}
        {% if forloop.index != 1 %}</ul>{% endif %}
            <h3>{{ post.date | date: '%B %Y' }}</h3><ul>
		{% endif %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
        <time>{{ post.date | date: "%e %B %Y" }}</time>
	{% endif %}]
	
	{% if forloop.last %}
	    </ul>
    {% endif %}
{% endfor %}