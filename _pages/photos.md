---
title: "ViBA - Photos"
layout: piclay
excerpt: "ViBA -- Photos"
permalink: /photos/
---


{% assign number_printed = 0 %}
{% for pic in site.data.pictures_Leiden %}

{% assign images_per_row = 3 %}
{% assign even_odd = number_printed | modulo: images_per_row %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}
<h5>{{ pic.title }}</h5>
<h6>{{ pic.date }}</h6>
<div class="col-sm-4 clearfix" height="400px" style="overflow: hidden;">
    <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="95%" style="float: left" />
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == images_per_row | minus: 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: images_per_row %}
{% if even_odd != 0 %}
</div>
{% endif %}

<p> &nbsp; </p>
