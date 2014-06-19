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
	<a class="post-title" href="{{ site.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
	<p class="post-description">{{ post.description }}...<a href="{{ site.url }}{{ post.url }}">阅读全文</a></p>
	<div class="post-time-line">
		<time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
	</div>
</div>
{% endfor %}