---
title: "ViBA - Journal"
layout: gridlay
excerpt: "ViBA -- Journal."
sitemap: false
permalink: /journal/
---


## Journal

{% for publi in site.data.journal %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
