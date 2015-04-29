---
layout: page
title: Blog Archive
permalink: blog/
---

{% for post in site.posts %}
  * {{ post.date | date_to_string }} &raquo; [ {{ post.title }} ]({{ post.url }})
{% endfor %}

---	  
>*&ldquo; Happiness is when what you think, what you say, and what you do are in harmony. &rdquo;*<br>&mdash; Mahatma Gandhi