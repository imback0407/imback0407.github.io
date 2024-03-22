---
title: "ViBA - Conference"
layout: gridlay
excerpt: "ViBA -- Conference."
sitemap: false
permalink: /conference/
---

## Conference

{% for publi in site.data.conference %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}

## Journal

{% for publi in site.data.journal %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
