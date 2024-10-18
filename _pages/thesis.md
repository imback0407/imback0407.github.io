---
title: "ViBA - Thesis"
layout: gridlay
excerpt: "ViBA -- Thesis."
sitemap: false
permalink: /thesis/
---

## Thesis

{% for publi in site.data.thesis %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}