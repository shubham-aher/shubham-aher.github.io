---
layout: page
title: Projects
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

	  
### Important Days - An Android App
*Know the most important days in a year.*


### Gajstotra - An Android App
*Recite Ganesh Stotras Daily.*


### PCAPFileAnalyzer
*Analyze PCAP Network Capture files.*


### HTTPLogFileAnalyzer
*Analyze an HTTP Log File.*


### NetMox
*A very simple Network Monitoring Tool.*


---	  
>*&ldquo; The severity of the itch is inversely proportional to the ability of scratching it. &rdquo;*<br>&mdash; Internet
