---
layout: default
title: Ken Booth
---

{% assign thedate = '' %}
<ul>
  {% for post in site.posts %}
 
  {% if thedate != post.date | date: "%m-%d-%Y" %}
        <h2>{{ post.date | date: "%A, %B %e, %Y" }}</h2>
  {% endif %}
  {% assign thedate = post.date | date: "%m-%d-%Y" %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>


