---
layout: default
title: Kursus
description: 
image-light: /assets/img/static/lamp-light.png
image-dark: /assets/img/static/lamp-dark.png
permalink: /courses/
---

<div class="container overflow-hidden pb-5">
	<div class="d-flex justify-content-center px-5 mt-n1">
		<img class="d-dark-mode-none" src="{{ page.image-light | relative_url }}" width="348" alt="{{ site.title }} - {{ page.title }}" style="transform-origin: 50% 0; animation: swinging 3.5s ease-in-out forwards infinite;">
		<img class="d-none d-dark-mode-block" src="{{ page.image-dark | relative_url }}" width="348" alt="{{ site.title }} - {{ page.title }}" style="transform-origin: 50% 0; animation: swinging 3.5s ease-in-out forwards infinite;">
	</div>
	<div class="d-flex justify-content-center pb-5 mb-md-2 mb-lg-3 mb-xl-4 mb-xxl-5">
		<div style="max-width: 420px;">
			<div class="d-none d-sm-block" style="margin-top: -127px;"></div>
			<div class="d-sm-none" style="margin-top: -25%;"></div>
			<div class="d-flex align-items-center mb-4">
				<h1 class="display-1 mb-0 text-center">Segera</h1>
			</div>
			<a class="btn btn-outline-dark w-100" href="{{ site.url }}">Kembali ke Halaman Utama</a>
		</div>
	</div>
</div>