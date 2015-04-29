---
layout: page
title: Project Archive
permalink: projects/
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
>*&ldquo; The severity of the itch is inversely proportional to the ability of scratching it. &rdquo;*<br>&mdash; Internet
