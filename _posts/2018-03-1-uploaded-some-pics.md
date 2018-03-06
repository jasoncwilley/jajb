---
layout: picture-post
title: "Some Pics From My Travels"
description: "I found some pics from my more recent travels so I thought I'd post them and try out a new layout I wrote for gallery posts."
tags: [picture, pictures, travels, trips, vacation, r and r, pictur-post layout]
comments: true
share: true
paginate: true
image:
  background: cube.png
---
{% assign images = include.images | split:" " %}
{% assign caption = include.caption %}
{% assign cols = include.cols %}

{% case cols %}
    {% when 1 %}
        {% assign class = "" %}
    {% when 2 %}
        {% assign class = "half" %}
    {% when 3 %}
        {% assign class = "third" %}
    {% else %}
        {% assign class = "" %}
{% endcase %}

<figure {% if class != "" %}class="{{ class }}"{% endif %}>
    {% for image in images %}
    <a href="{{ image }}"><img src="{{ image }}" alt=""></a>
    {% endfor %}
    <figcaption>{{ caption }}</figcaption>
</figure>
