---
layout: page
title: Juggling
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
###Coming Soon !
---	  
