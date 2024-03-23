---
title: "ViBA - Project"
layout: gridlay
excerpt: "ViBA -- projects."
sitemap: false
permalink: /projects/
---

## Projects

{% assign number_printed = 0 %}
{% for publi in site.data.project %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
    <div class="well">
        <pubtit>{{ publi.title }}</pubtit>
        <p>{{ publi.organization }} / <em>{{ publi.date }}</em></p>
        <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" style="width: 33%; max-height: 80%; float: left;">
        <p>{{ publi.description }}</p>
    </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>
