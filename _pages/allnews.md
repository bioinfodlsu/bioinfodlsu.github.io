---
title: "News"
layout: textlay
excerpt: "Allan Lab at Leiden University."
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
{{ article.date }}
{{ article.headline | markdownify}}
{% if article.pic != nil %}
<img src="images/news/{{ article.pic }}" width=350 >
{% endif %}
----
{% endfor %}
