---
title: "ViBA - Courses"
layout: gridlay
excerpt: "ViBA : Courses"
sitemap: false
permalink: /courses/
---

## Courses
<p> &nbsp; </p>

{% assign number_printed = 0 %}
{% for course in site.data.courses %}
<div class="row" width = "100%" style="text-align: left;">
{% assign even_odd = number_printed | modulo: 2 %}

<p>‣ <b>{{ course.title }}</b> {{ course.code }} (<em>{{ course.date }}</em>)</p>

{% assign number_printed = number_printed | plus: 1 %}
</div>
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}

<p> &nbsp; </p>
