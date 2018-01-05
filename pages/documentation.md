---
layout: page
title: Blogs
---
{% for post in site.categories.documentation %}
<div>
	<a href="{{ site.github.url }}{{ post.url }}">
	  <div class="featured-posts" {% if post.image %}style="background-image:url({{ site.github.url }}/gallery/{{post.date | date:"%Y/%m/%d/" }}{{post.date | date:"%Y%m%d-" }}{{ post.image }})"{% endif %}>
	      <h2><span>{{ post.title }}</span></h2>
	  </div>
	</a>
</div>
{% endfor %}
