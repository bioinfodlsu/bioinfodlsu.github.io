---
title: "Bioinfo Lab - Publications"
layout: gridlay
excerpt: "Bioinfo Lab -- Publications."
sitemap: false
permalink: /publications/
---

### Journal articles and conference presentations

<!--
{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
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

## Full List of publications
-->

{% assign publi_grouped = site.data.publist | sort: "year" | reverse | group_by: "year" %}
{% for group in publi_grouped %}
<h4>{{group.name}}</h4>
{% for publi in group.items %}

<div class="row flex">
<div class="col-auto flex pub-pic">
<img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="pub-img" />
</div>
<div class="col-sm-10 flex pub-text">
{% if publi.link.url %}<a href="{{ publi.link.url }}" target="_blank">{{ publi.title }}</a> {% else %}{{ publi.title }}{% endif %}
<br /><em>{{ publi.authors }} </em><br />{{ publi.link.display }}
{{publi.no-link}}
</div>
</div>

{% endfor %}
{% endfor %}
