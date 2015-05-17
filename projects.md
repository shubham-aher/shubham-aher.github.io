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

This app gives you the list of famous days that are celebrated throughout the world.<br>
Get it free from: [https://play.google.com/store/apps/details?id=com.shubhamaher.importantdays](https://play.google.com/store/apps/details?id=com.shubhamaher.importantdays)

### Gajstotra - An Android App
*Recite Ganesh Stotras Daily.*

GajStotra is your devotional companion app to learn the most important "stotras" of Hindu religion, the Gajanan(Ganesh) Stotra.
Get it free from: [https://play.google.com/store/apps/details?id=shubham.aher.gajstotra](https://play.google.com/store/apps/details?id=shubham.aher.gajstotra)

### PCAPFileAnalyzer
*Analyze PCAP Network Capture files.*

Source Code at: [https://github.com/shubham-aher/PCAPFileAnalyzer](https://github.com/shubham-aher/PCAPFileAnalyzer)

### HTTPLogFileAnalyzer
*Analyze an HTTP Log File.*

Source Code at: [https://github.com/shubham-aher/HTTPLogFileAnalyzer](https://github.com/shubham-aher/HTTPLogFileAnalyzer)

### NetMox
*A very simple Network Monitoring Tool.*

Source Code at: [https://github.com/shubham-aher/netmox](https://github.com/shubham-aher/netmox)

---	  
>*&ldquo; The severity of the itch is inversely proportional to the ability of scratching it. &rdquo;*<br>&mdash; Internet
