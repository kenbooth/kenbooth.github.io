---
layout: default
title: Ken Booth
---

{% for post in site.posts %}
  {% capture currentdate %}{{post.date | date: "%A, %B %d, %Y"}}{% endcapture %}
  {% if currentdate != thedate %}
    <h2>{{ currentdate }}</h2>
    {% capture thedate %}{{currentdate}}{% endcapture %} 
  {% endif %}
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
	{% endfor %}


