---
layout: page
title: Gallery
---
{% for post in site.categories.documentation %}
<img class="featured-posts" src="{{ site.github.url }}/gallery/{{post.date | date:"%Y/%m/%d/" }}{{post.date | date:"%Y%m%d-" }}{{ post.image }}"/>
{% endfor %}
