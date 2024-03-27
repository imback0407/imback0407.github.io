---
title: "ViBA - Courses"
layout: gridlay
excerpt: "ViBA : Courses"
sitemap: false
permalink: /courses/
---
## Courses 
<p> &nbsp;</p>

{% assign number_printed = 0 %}
{% for course in site.data.courses %}

{% assign even_odd = number_printed | modulo: 2 %}
<h7>‣ <b>{{ course.title }}</b> {{ course.code }} (<em>{{ course.date }}</em>) &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;</h7>

{% assign number_printed = number_printed | plus: 1 %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}

<p> &nbsp; </p>
