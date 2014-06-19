---
title: 王文壮的博客 - Code
layout: page
---
<script type="text/javascript">
	$(function () {
		$('#nav3').addClass('active');
	});
</script>
<div>
{% for post in site.categories.code %}
	<div>
		<a class="post-title" href="{{ site.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
		<p class="post-description">{{ post.description }}...<a href="{{ site.url }}{{ post.url }}">阅读全文</a></p>
		<div class="post-time-line">
			<time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
			&nbsp;&nbsp;|&nbsp;&nbsp;<a href="{{ site.url }}">{{ site.author }}</a>
		</div>
	</div>
{% endfor %}
</div>