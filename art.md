---
layout: full-width
title: Art
description: We become the things we do
og_title: Self-mastery | Taylor McKnight
og_description: We become the things we do
og_image: /media/img/about/mcknight_headshot.jpg
og_type: website
---
<section class="grid page-header">
	<div class="full-width">
		<h1>{{ page.title }}</h1>
		<p>&ldquo;Art is a therapeutic medium that can help guide, exhort and console its viewers, enabling them to become better verisons of themselves&rdquo; – Alain de Botton</p>
	</div>
</section>

<section class="stripe-section-2">
	<section class="grid-wrapper feed">
		{% for art in site.categories.art %}
		<article>
			<figcaption>
				{% if art.external_url %}
				<a href="{{ art.external_url }}">
				{% else %}
				<a href="{{ art.url }}">
				{% endif %}
				<h3>
					{{ art.title }}
				</h3>
				</a>
				<p class="description">{{ art.description }}</p>
				<p>
				{% if art.external_url %}
				<a href="{{ art.external_url }}">
				{% else %}
				<a href="{{ art.url }}">
				{% endif %}
				Read more
				{% if art.external_url %}
				<img src="{{ site.url }}/media/img/external-link-icon.png" class="external-link-icon">
				{% endif %}
				</a>
				</p>
			</figcaption>
			{% if art.image %}
			<figure>
				{% if art.external_url %}
				<a href="{{ art.external_url }}">
				{% else %}
				<a href="{{ art.url }}">
				{% endif %}
				<img src="{{ art.image }}" />
				</a>
			</figure>
			{% endif %}
		</article>
		{% endfor %}
	</section>
</section>