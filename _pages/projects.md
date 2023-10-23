---
title: "Bioinfo Lab - Projects"
layout: gridlay
excerpt: "Bioinfo Lab: Projects"
sitemap: false
permalink: /projects/
---

# Projects
Here are some ongoing and past projects.

{% for proj in site.data.projs %}

<div class="row">

<div class="clearfix well proj-item-container">
  <pubtit>{{ proj.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ proj.image }}" class="img-responsive" width="20%" style="float: left" />
  <p>{{ proj.description }}</p>
</div>

</div>

{% endfor %}
