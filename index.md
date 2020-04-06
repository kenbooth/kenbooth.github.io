---
layout: default
title: Ken Booth
---

{% assign thedate = '' %}

{% for post in paginator.posts %}

    {% if thedate != post.date | date: "%m-%d-%Y" %}
        <h2>{{ post.date | date: "%A, %B %e, %Y" }}</h2>
    {% endif %}

    {% assign thedate = post.date | date: "%m-%d-%Y" %}

    <h3 class="headline"><a href="{{ post.url }}">{{ post.title }}</a></h3>
    {{ post.content }}
    <hr>

{% endfor %}


{% for post in paginator.posts %}
  <h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
  <p class="author">
    <span class="date">{{ post.date }}</span>
  </p>
  <div class="content">
    {{ post.content }}
  </div>
{% endfor %}