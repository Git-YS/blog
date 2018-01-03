---
layout: page
title: Tags
---

&ensp;{% for tag in site.tags %} {{ tag[0] }} {% endfor %}
{% for tag in site.tags %}
&emsp;&emsp;&emsp;&emsp;{{ tag[0] }}
{% for post in tag[1] %}
&emsp;&emsp;{{ post.date | date:"%Y-%m-%d" }}&emsp;&emsp;<a href="{{ site.github.url }}{{ post.url }}">{{ post.title }}</a>
{% endfor %} {% endfor %}
<script src="//cdnjs.cloudflare.com/ajax/libs/jquery/3.2.1/jquery.min.js" type="text/javascript" charset="utf-8"></script> 
<script src="../assets/js/jquery-tagCloud.js" type="text/javascript" charset="utf-8"></script> 
<script type="text/javascript">
	$.fn.tagcloud.defaults = { size: {start: 1, end: 1, unit: 'em'}, color: {start: '#f8e0e6', end: '#ff3333'} }; 
	$(function () { $('#tag_cloud a').tagcloud(); }); 
</script>