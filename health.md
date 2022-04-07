---
layout: full-width
title: Health &amp; Wellbeing
description: Reflections on how to improve human health and wellbeing
og_title: Health &amp; Wellbeing | Taylor McKnight
og_description:  Reflections on how to improve human health and wellbeing
og_image: /media/img/about/mcknight_headshot.jpg
og_type: website
---
<section class="grid page-header">
	<div class="full-width">
		<h1>{{ page.title }}</h1>
		<p>&ldquo;A healthy man wants a thousand things, a sick man only wants one.&rdquo; – Confucius</p>
	</div>
</section>
<section class="stripe-section-2">
	<section class="grid-wrapper feed">
		{% for health in site.categories.health %}
		<article>
			<figcaption>
				{% if health.external_url %}
				<a href="{{ health.external_url }}">
				{% else %}
				<a href="{{ health.url }}">
				{% endif %}
				<h3>
					{{ health.title }}
				</h3>
				</a>
				<p class="label">{{ health.date | date: "%-d %B %Y" }}</p>
				<p class="description">{{ health.description }}</p>
				<p>
				{% if health.external_url %}
				<a href="{{ health.external_url }}">
				{% else %}
				<a href="{{ health.url }}">
				{% endif %}
				Read more
				</a>
				</p>
			</figcaption>
			{% if health.image %}
			<figure>
				{% if health.external_url %}
				<a href="{{ health.external_url }}">
				{% else %}
				<a href="{{ health.url }}">
				{% endif %}
				<img src="{{ health.image }}" />
				</a>
			</figure>
			{% endif %}
		</article>
		{% endfor %}
	</section>
</section>
