---
title: "ViBA - Alumni"
layout: gridlay
excerpt: "ViBA: Alumni"
sitemap: false
permalink: /alumni/
---

<h2>Alumni</h2>

{% assign number_printed = 0 %}
<div class="row"> 
{% for member in site.data.alumni_members %}

{% assign even_odd = number_printed | modulo: 2 %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" style="width: 150px; height: 210px; object-fit: cover; float: left;" />
  <h4>{{ member.name }}</h4>
  <h5>Current Status : {{ member.current_status }}</h5>
  <i>{{ member.duration }} <br>email: <{{ member.email }}></i>
  <ul style="overflow: hidden">

    {% for i in (1..member.number_educ) %}
    <li>{{ member["education" | append: i] | markdownify }}</li>
    {% endfor %}

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div><div class="row"> 
{% endif %}

{% endfor %}
</div> 
