---
layout: page
title: Juggling Archive
permalink: juggling/
---
      {% assign pages_list = site.pages | sort:"name" %}
      {% for node in pages_list reversed %}
        {% if node.title != null %}
          {% if node.layout == "project" %}
  * {{ node.date | date_to_string }} &raquo; [ {{ node.title }} ]({{ node.url }}) <br /> {{ node.description }}
          {% endif %}
        {% endif %}
      {% endfor %}

---	  
>*&ldquo; <a href="http://en.wikipedia.org/wiki/Passing_(juggling)" target="_blank">Passing clubs</a> is one of the most funniest things two people can do without taking their clothes off &rdquo;*<br>&mdash; Isaac Orr