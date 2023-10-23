---
title: "Bioinfo Lab - Projects"
layout: gridlay
excerpt: "Bioinfo Lab: Projects"
sitemap: false
permalink: /projects/
---

# Projects
Here are some ongoing and past projects.

{% assign number_printed = 0 %}
{% for proj in site.data.projs %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if proj.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ proj.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ proj.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ proj.description }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>
