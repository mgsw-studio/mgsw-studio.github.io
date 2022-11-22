---
layout: default
title: Blog
permalink: /blog/
---

<div class="container pt-5 pb-lg-5 pb-md-4 pb-2 my-5">
	<nav aria-label="breadcrumb">
		<ol class="pt-lg-3 pb-lg-4 pb-2 breadcrumb">
			<li class="breadcrumb-item"><a href="{{ site.baseurl }}">{{ site.title }}</a></li>
			<li class="breadcrumb-item active" aria-current="page">{{ page.title }}</li>
		</ol>
	</nav>
	<div class="row align-items-center gy-2 mb-4 pb-1 pb-sm-2 pb-lg-3">
		<div class="col-lg-5">
			<h1 class="mb-lg-0">{{ page.title }}</h1>
		</div>
	</div>
	{% for post in site.posts limit: 9 %}
	<article class="row g-0 border-0 mb-5">
		<a class="col-sm-5 col-lg-4 bg-repeat-0 bg-size-cover bg-position-center rounded" href="{{ post.url }}" style="background-image: url({{ post.thumbnail-image | relative_url }}); min-height: 16rem"></a>
		<div class="col-sm-7 col-lg-8">
			<div class="pt-4 pb-sm-4 ps-sm-4 pe-lg-4">
				<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
				<p class="d-sm-none d-md-block">{{ post.excerpt | strip_html | truncatewords:30 }}</p>
				<div class="d-flex flex-wrap align-items-center mt-n2">
					<span class="fs-sm text-muted mt-2">{{ post.date | date_to_long_string }}</span>
					<span class="fs-xs opacity-20 mt-2 mx-3">|</span>
					<a class="badge text-nav fs-xs border mt-2">{{ post.author }}</a>
				</div>
			</div>
		</div>
	</article>
	{% endfor %}
</div>