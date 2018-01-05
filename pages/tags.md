---
layout: page
title: Tags
---

<div id='tag_cloud'>
&emsp;{% for tag in site.tags %}
<a href="#{{ tag[0] }}" title="{{ tag[0] }}" rel="{{ tag[1].size }}">{{ tag[0] }}</a>
{% endfor %}
</div>

<ul class="listing">
{% for tag in site.tags %}
  <p class="listing-seperator" id="{{ tag[0] }}">&emsp;&emsp;{{ tag[0] }}</p>
{% for post in tag[1] %}
  <li class="listing-item">
  <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time> 
  <a href="{{ post.url }}" title="{{ post.title }}">&emsp;{{ post.title }}</a>
  </li>
{% endfor %}
{% endfor %}
</ul>

<script src="//cdnjs.cloudflare.com/ajax/libs/jquery/3.2.1/jquery.min.js" type="text/javascript" charset="utf-8"></script>
<script src="/assets/js/jquery-tagcloud.js" type="text/javascript" charset="utf-8"></script> 
<script language="javascript">
$.fn.tagcloud.defaults = {
    size: {start: 1, end: 1, unit: 'em'},
      color: {start: '#BDD9FF', end: '#3389FF'}
};

$(function () {
    $('#tag_cloud a').tagcloud();
});
</script>