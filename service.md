---
layout: full-width
title: Service
description: Reflections on my startup and business experiences
og_title: Startup Journal | Taylor McKnight
og_description: Reflections on my startup and business experiences
og_image: /media/img/about/mcknight_headshot.jpg
og_type: website
---
<section class="grid page-header">
	<div class="full-width">
		<h1>{{ page.title }}</h1>
		<p>Community is not free.</p>
	</div>
</section>
<section class="stripe-section-2">
	<section class="grid-wrapper feed">
		{% for service in site.categories.service %}
		<article>
			<figcaption>
				{% if service.external_url %}
				<a href="{{ service.external_url }}">
				{% else %}
				<a href="{{ service.url }}">
				{% endif %}
				<h3>
					{{ service.title }}
				</h3>
				</a>
				<p class="label">{{ service.date | date: "%-d %B %Y" }}</p>
				<p class="description">{{ service.description }}</p>
				<p>
				{% if service.external_url %}
				<a href="{{ service.external_url }}">
				{% else %}
				<a href="{{ service.url }}">
				{% endif %}
				Read more
				</a>
				</p>
			</figcaption>
			{% if service.image %}
			<figure>
				{% if service.external_url %}
				<a href="{{ service.external_url }}">
				{% else %}
				<a href="{{ service.url }}">
				{% endif %}
				<img src="{{ service.image }}" />
				</a>
			</figure>
			{% endif %}
		</article>
		{% endfor %}
	</section>
</section>
