---
title: "ViBA - Alumni"
layout: gridlay
excerpt: "ViBA: Alumni"
sitemap: false
permalink: /alumni/
---

# Alumni

{% assign number_printed = 0 %}
{% for member in site.data.alumni_members %}

{% assign even_odd = number_printed | modulo: 2 %}


<div class="col-sm-12 clearfix">
  <h4>{{ member.name }} &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;</h4>
  <h7>{{ member.duration }}</h7>
</div>

{% assign number_printed = number_printed | plus: 1 %}


{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
