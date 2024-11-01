---
title: "ViBA - Photos"
layout: piclay
excerpt: "ViBA -- Photos"
permalink: /photos/
---

<h2>Photos</h2>
<p> &nbsp; </p>
<div class="photo-gallery" style="display: flex; flex-wrap: wrap; gap: 20px; justify-content: space-around;">
  {% assign number_printed = 0 %}
  {% for pic in site.data.pictures %}

    <div class="photo-item" style="text-align: center; width: 270px;">
      <div class="photo-info" style="height: 80px; display: flex; flex-direction: column; justify-content: center;">
        <h5 style="margin: 0;">{% if pic.title == "" %}Lab Pic{% else %}<b>{{ pic.title }}</b>{% endif %}</h5>
        <h6 style="margin: 0;">{% if pic.date == "" %}YYYY.MM.DD{% else %}{{ pic.date }}{% endif %}</h6>
      </div>
      <img src="{{ site.url }}{{ site.baseurl }}/images/picpic/Gallery/{{ pic.image }}" class="img-responsive" style="width: 100%; height: 350px; object-fit: cover;" />
    </div>

    {% assign number_printed = number_printed | plus: 1 %}
  {% endfor %}
</div>

<p> &nbsp; </p>
<p> &nbsp; </p>