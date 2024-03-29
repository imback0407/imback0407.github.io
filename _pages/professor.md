---
title: "ViBA - Professor"
layout: gridlay
excerpt: "ViBA: Professor"
sitemap: false
permalink: /professor/
---

<h2>Professor</h2>

{% assign number_printed = 0 %}
{% for member in site.data.team_professor %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-12 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <div class="col-md-9">
        <hr class="w-25 d-md-none d-lg-none d-xl-none d-xxl-none">
        <h2 class="mb-3"><i class="bi-chat-left-text me-3"></i> Bio</h2>
        <p>Hyunwoo Park is an Associate Professor in the Graduate School of Data Science at Seoul National University. Before joining SNU, he was an Assistant Professor in Management Sciences at the Fisher College of Business and a Core Faculty for the Translational Data Analytics Institute (TDAI) at The Ohio State University. Prior to OSU, he was a postdoctoral fellow at the Tennenbaum Institute at Georgia Tech. He holds a Ph.D. in Industrial Engineering from Georgia Tech, a Master of Information Management and Systems from UC Berkeley, and a B.S. in Electrical Engineering from Seoul National University.</p>
        <p>His research interests include business and data analytics with an emphasis on visualization, supply chain management from the network perspective, and technology and innovation management in the presence of digital platforms.</p>
        <p>His research has been published in leading journals including Academy of Management Review, Decision Sciences, Decision Support Systems, IEEE Transactions on Engineering Management (TEM), IEEE Transactions on Visualization and Computer Graphics (TVCG), Journal of Operations Management, and Research Policy.</p>
        <p>He won the TIM (Technology and Innovation Management) Division Best Student Paper Award at the Academy of Management in 2015 and the OCIS (Organizational Communication and Information Systems) Division Best Paper Award at the Academy of Management in 2017. His paper was a finalist for the Chan Hahn Best Paper Award in the OSCM (Operations and Supply Chain Management) Division at the Academy of Management in 2020. His dissertation was awarded a Runner-up for the INFORMS TIMES (Technology, Innovation Management and Entrepreneurship Section) Best Dissertation Award in 2017.</p>
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
