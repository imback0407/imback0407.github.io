---
title: "ViBA - Photos"
layout: piclay
excerpt: "ViBA -- Photos"
permalink: /photos/
---

<h2>Photos</h2>
<p> &nbsp; </p>
{% assign number_printed = 0 %}
{% for pic in site.data.pictures %}

{% assign even_odd = number_printed | modulo: 4 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-3 clearfix" style="text-align: left;">
  <h5 style="text-align: left; height: 30px">{% if pic.title == "" %}Lab Pic{% else %}<b>{{ pic.title }}</b>{% endif %}</h5>

  <div style="width: 270px; display: flex; align-items: center; justify-content: center; margin: 10px 0;">
    <div style="flex: 1; height: 2px; background-color: #ccc;"></div> <!-- 左边直线 -->
    <div style="width: 8px; height: 8px; background-color: #333; border-radius: 50%; margin: 0 10px;"></div> <!-- 中心圆点 -->
    <div style="flex: 1; height: 2px; background-color: #ccc;"></div> <!-- 右边直线 -->
  </div>
  
  <h6 style="text-align: left;">{% if pic.date == "" %}YYYY.MM.DD{% else %}{{ pic.date }}{% endif %}</h6>
  <img src="{{ site.url }}{{ site.baseurl }}/images/picpic/Gallery/{{ pic.image }}" class="img-responsive" style="width:270px; height:350px; object-fit: cover; text-align: left;" />
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd > 2 %}
</div>
{% endif %}
{% endfor %}
{% assign even_odd = number_printed | modulo: 4 %}
{% if even_odd == 1 %}
</div>
{% endif %}

{% if even_odd == 2 %}
</div>
{% endif %}

{% if even_odd == 3 %}
</div>
{% endif %}

<p> &nbsp; </p>
<p> &nbsp; </p>
