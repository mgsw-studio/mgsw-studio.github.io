---
layout: page
title: Projek
description: Apa saja yang bisa kami lakukan dan sudah kami kerjakan?
permalink: /project/
---

<div class="container overflow-hidden">
	<div class="masonry-filterable">
		<div class="row pb-lg-4 mb-2 mb-sm-3">
			<div class="col-xxl-9 col-lg-8 d-flex mx-auto">
				{% assign filter-item = site.data.filter.filter-project %}
				<ul class="masonry-filters nav nav-pills fs-sm flex-nowrap overflow-auto text-nowrap w-100 mx-auto me-lg-0 pb-3">
					{% for item in filter-item %}
						<li class="nav-item mb-0"><a class="nav-link border {% if item == name %} active {% endif %}" href="#" data-group="{{ item.data-group }}">{{ item.name }}</a></li>
					{% endfor %}
				</ul>
			</div>
		</div>
		{% if site.data.project %}
		<div class="masonry-grid" data-columns="3">
			{% assign projects = site.data.project | sort: 'year' %}
			{% for item in projects %}
			<article class="masonry-grid-item pb-5 mb-md-2 mb-lg-4 mb-xl-5" data-groups='["{{ item.data-group }}"]'>
				<div class="zoom-effect position-relative border-bottom pb-3" style="max-width: 512px;">
					<div class="zoom-effect-wrapper">
						<div class="zoom-effect-img"><img src="{{ item.project-thumbnail | relative_url }}" alt="{{ item.client-name }}"></div>
					</div>
					<div class="pt-4 mt-lg-2">
						<h2 class="h4 mb-2"><a class="stretched-link" href="{{ item.url | relative_url }}">{{ item.client-name }}</a></h2>
						<div class="d-flex justify-content-between fs-lg text-muted">
							<span>{{ item.category }}</span>
							<span>{{ item.year }}</span>
						</div>
					</div>
				</div>
			</article>
			{% endfor %}
		{% endif %}
		</div>
	</div>
</div>