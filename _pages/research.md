---
title: "CNDL@IITJ - Research"
layout: gridlay
sitemap: false
permalink: /research/
---

## Research

<div class="row">

{% assign sorted_research = site.data.research %}
{% for item in sorted_research %}

  <div class="col-sm-6 clearfix">
    <div class="well">
      <pubtit>{{ item.title }}</pubtit>
      {% if item.image and item.image != "" %}
        <img src="{{ item.image }}" class="img-responsive" width="80%" style="float: center; margin-bottom: 10px;" />
      {% endif %}
      {% if item.question %}
        <p><b>Question:</b> {{ item.question }}</p>
      {% endif %}
      <p>{{ item.description }}</p>
      {% if item.link_url and item.link_url != "" %}
        <p><strong><a href="{{ item.link_url }}">{{ item.link_display }}</a></strong></p>
      {% endif %}
    </div>
  </div>

  {% assign mod = forloop.index | modulo: 2 %}
  {% if mod == 0 %}
    </div><div class="row">
  {% endif %}

{% endfor %}

</div> <!-- closing row -->