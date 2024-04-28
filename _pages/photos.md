---
title: "ViBA - Photos"
layout: piclay
excerpt: "ViBA -- Photos"
permalink: /photos/
---

<h2>Photos</h2>
<p>&nbsp;</p>
{% assign number_printed = 0 %}
{% assign images_per_row = 3 %}
<div class="row">
{% for pic in site.data.pictures_Leiden %}
    <div class="col-sm-4 clearfix" style="max-width: 320px;">
      <h4>{{ pic.title }}</h4>
      <h6>{{ pic.date }}</h6>
      <img src="{{ site.url }}{{ site.baseurl }}/images/picpic/Gallery/{{ pic.image }}" class="img-responsive" style="width:270px; height:350px; object-fit: cover;" />
    </div>
    {% assign number_printed = number_printed | plus: 1 %}
    {% if number_printed | modulo: images_per_row == 0 and forloop.last == false %}
        </div><div class="row">
    {% endif %}
{% endfor %}
</div>
<p>&nbsp;</p>
