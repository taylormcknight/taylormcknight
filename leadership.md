---
layout: full-width
title: Leadership
description: Posts about leadership and management
og_title: Leadership and management | Taylor McKnight
og_description:  Posts about leadership and management
og_image: /media/img/about/headshot-2022.jpg
og_type: website
---
<section class="grid page-header">
	<div class="full-width">
		<h1>{{ page.title }}</h1>
		<p>Always open. Always learning.</p>
	</div>
</section>
<section class="stripe-section-2">
	<section class="grid-wrapper feed">
		{% for leadership in site.categories.leadership %}
		<article>
			<figcaption>
				{% if leadership.external_url %}
				<a href="{{ leadership.external_url }}">
				{% else %}
				<a href="{{ leadership.url }}">
				{% endif %}
				<h3>
					{{ leadership.title }}
				</h3>
				</a>
				<p class="label">{{ leadership.date | date: "%-d %B %Y" }}</p>
				<p class="description">{{ leadership.description }}</p>
				<p>
				{% if leadership.external_url %}
				<a href="{{ leadership.external_url }}">
				{% else %}
				<a href="{{ leadership.url }}">
				{% endif %}
				Read more
				{% if leadership.external_url %}
				<img src="{{ site.url }}/media/img/external-link-icon.png" class="external-link-icon">
				{% endif %}
				</a>
				</p>
			</figcaption>
			{% if leadership.image %}
			<figure>
				{% if leadership.external_url %}
				<a href="{{ leadership.external_url }}">
				{% else %}
				<a href="{{ leadership.url }}">
				{% endif %}
				<img src="{{ leadership.image }}" />
				</a>
			</figure>
			{% endif %}
		</article>
		{% endfor %}
	</section>
</section>
