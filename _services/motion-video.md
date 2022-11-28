---
layout: page
title: Motion & Video
description: Tampilkan dan berikan yang terbaik untuk produk ataupun bisnis Anda kepada calon konsumen melalui jasa video dari kami.
featured-img: assets/img/services/motion-video-loop.gif
services-img: assets/img/services/cup-loop.gif
permalink: /motion-video/
---

<section class="container py-4 py-sm-5 my-md-2 my-lg-3 my-xl-4 my-xxl-5">
	<div class="row align-items-center py-4 py-xl-5 my-2">
		<div class="col-md-6 offset-xl-1 order-md-2 pb-2 mb-4 mb-md-0">
			<img class="rounded border" src="{{ page.services-img | relative_url }}" alt="{{ page.title }}">
		</div>
		<div class="col-md-6 col-xl-5 order-md-1">
			<div class="pe-md-4 pe-xl-0">
				<div class="row row-cols-2">
					{% if site.data.services %}
						{% for item in site.data.services.motion-video %}
						<div class="col mb-5">
							<div class="d-table bg-secondary rounded-1 p-2 mb-3">
								<img class="d-block d-dark-mode-none m-1" src="{{ item.service-icon-dark | relative_url }}" width="28" alt="Icon">
								<img class="d-none d-dark-mode-block m-1" src="{{ item.service-icon-light | relative_url  }}" width="28" alt="Icon">
							</div>
							<h3 class="h5 mb-2">{{ item.service-name }}</h3>
							<p class="fs-sm mb-0">{{ item.service-description }}</p>
						</div>
						{% endfor %}
					{% endif %}
					<a class="btn btn-outline-dark btn-lg mx-auto" href="/pricing/">Lihat Daftar Harga</a>
				</div>
			</div>
		</div>
	</div>
</section>
<section class="container py-4 py-sm-5 my-md-2 my-lg-3 my-xl-4 my-xxl-5">
	<h2 class="h1 text-center">Bermitra dengan lebih dari 10 lebih bisnis</h2>
	<p class="text-center pb-2 pb-sm-3">Kami senantiasa menanti Anda juga untuk bergabung untuk menjadi salah satu mitra kami.</p>
    {% assign clients = site.data.home.client-logo | sort: 'name' %}
	<div class="row row-cols-2 row-cols-md-4 g-2 g-md-4">
		{% for item in clients %}
		<div class="col">
			<img class="d-block d-dark-mode-none mx-auto mb-3" src="{{ item.logo-dark | relative_url }}" width="{{ item.width }}" alt="{{ item.name }}" data-bs-container="body" data-bs-toggle="popover" data-bs-placement="top" data-bs-trigger="hover" data-bs-content="{{ item.name }}">
			<img class="d-none d-dark-mode-block mx-auto mb-3" src="{{ item.logo-light | relative_url }}" width="{{ item.width }}" alt="{{ item.name }}" data-bs-container="body" data-bs-toggle="popover" data-bs-placement="top" data-bs-trigger="hover" data-bs-content="{{ item.name }}">
		</div>
		{% endfor %}
	</div>
</section>
{% include cta.html %}