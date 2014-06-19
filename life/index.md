---
title: 王文壮的博客 - 生活
layout: page
---
<script type="text/javascript">
	$(function () {
		$('#nav2').addClass('active');
	});
</script>
{% for post in site.categories.life %}
<div>
	<a class="page-title" href="{{ site.url }}{{ post.url }}" title="{{ post.title }}" target="_blank">{{ post.title }}</a>
	<p class="page-description">{{ post.description }}...<a href="{{ site.url }}{{ post.url }}" target="_blank">阅读全文</a></p>
	<div class="page-time-line">
		<time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
	</div>
</div>
{% endfor %}