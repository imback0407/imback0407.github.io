---
title: "ViBA - Members"
layout: gridlay
excerpt: "ViBA: Members"
sitemap: false
permalink: /members/
---

 <!--**We are  looking for new PhD students, Postdocs, and Master students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/vacancies) **!**-->

<h2>PhD / Ms - Ph.D Integrated</h2>

{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
<img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" style="width: 150px; height: 210px; object-fit: cover; float: left;" />
  <h4>{{ member.name }}</h4>
  <h5>Research Interest : {{ member.research }}</h5>
  <i>{{ member.info }} <br>email: <{{ member.email }}></i>
  <ul style="overflow: hidden">

  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 | markdownify}} </li>
  <li> {{ member.education2 | markdownify}} </li>
  {% endif %}

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}

  {% if member.number_educ == 5 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  <li> {{ member.education5 }} </li>
  {% endif %}

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
<div style="clear: both;"></div>
{% endif %}
{% endfor %}

{% if number_printed | modulo: 2 == 1 %}
</div>
<div style="clear: both;"></div>
{% endif %}

<h2>Masters</h2>

{% assign number_printed = 0 %}
{% for member1 in site.data.team_members_master %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}

<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
<img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member1.photo }}" class="img-responsive" style="width: 150px; height: 210px; object-fit: cover; float: left;"/>
  <h4>{{ member1.name }}</h4>
  <h5>Research Interest : {{ member1.research }}</h5>
  <i>{{ member1.info }} <br>email: <{{ member1.email }}></i>
  <ul style="overflow: hidden">

  {% if member1.number_educ == 1 %}
  <li> {{ member1.education1 }} </li>
  {% endif %}

  {% if member1.number_educ == 2 %}
  <li> {{ member1.education1 | markdownify}} </li>
  <li> {{ member1.education2 | markdownify}} </li>
  {% endif %}

  {% if member1.number_educ == 3 %}
  <li> {{ member1.education1 }} </li>
  <li> {{ member1.education2 }} </li>
  <li> {{ member1.education3 }} </li>
  {% endif %}

  {% if member1.number_educ == 4 %}
  <li> {{ member1.education1 }} </li>
  <li> {{ member1.education2 }} </li>
  <li> {{ member1.education3 }} </li>
  <li> {{ member1.education4 }} </li>
  {% endif %}

  {% if member1.number_educ == 5 %}
  <li> {{ member1.education1 }} </li>
  <li> {{ member1.education2 }} </li>
  <li> {{ member1.education3 }} </li>
  <li> {{ member1.education4 }} </li>
  <li> {{ member1.education5 }} </li>
  {% endif %}

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
<div style="clear: both;"></div>
{% endif %}
{% endfor %}

{% if number_printed | modulo: 2 == 1 %}
</div>
<div style="clear: both;"></div>
{% endif %}
