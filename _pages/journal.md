---
title: "VIBA - Journal"
layout: gridlay
excerpt: "VIBA -- Journal."
sitemap: false
permalink: /journal/
---


## Full List of Journal

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
