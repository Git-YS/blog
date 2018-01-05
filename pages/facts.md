---
layout: page
title: Gallery
---
{% for post in site.categories.gallery %}
<div>
	<a href="{{ site.github.url }}{{ post.url }}">
	  <img class="featured-posts" src="{{ site.github.url }}/gallery/{{post.date | date:"%Y/%m/%d/" }}{{post.date | date:"%Y%m%d-" }}{{ post.title }}"/>
	</a>
</div>
{% endfor %}
