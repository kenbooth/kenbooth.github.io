---
layout: default
title: Ken Booth
---

{% for post in site.posts %}
  {% capture currentdate %}{{post.date | date: "%A, %B %d, %Y"}}{% endcapture %}
  {% if currentdate != thedate %}
    {{ currentdate }}
    {% capture thedate %}{{currentdate}}{% endcapture %} 
  {% endif %}
   <a href="{{ post.url }}">{{ post.title }}. {{ post.excerpt }}</a>
{% endfor %}


