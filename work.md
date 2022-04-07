---
layout: full-width
title: Work
description: Reflections on my startup and business experiences
og_title: Startup Journal | Taylor McKnight
og_description: Reflections on my startup and business experiences
og_image: /media/img/about/mcknight_headshot.jpg
og_type: website
---
<section class="grid page-header">
	<div class="full-width">
		<h1>{{ page.title }}</h1>
		<p>We become the things we do.</p>
	</div>
</section>
<section class="stripe-section-2">
	<section class="grid-wrapper feed">
		{% for work in site.categories.work %}
		<article>
			<figcaption>
				{% if work.external_url %}
				<a href="{{ work.external_url }}">
				{% else %}
				<a href="{{ work.url }}">
				{% endif %}
				<h3>
					{{ work.title }}
				</h3>
				</a>
				<p class="label">{{ work.date | date: "%-d %B %Y" }}</p>
				<p class="description">{{ work.description }}</p>
				<p>
				{% if work.external_url %}
				<a href="{{ work.external_url }}">
				{% else %}
				<a href="{{ work.url }}">
				{% endif %}
				Read more
				</a>
				</p>
			</figcaption>
			{% if work.image %}
			<figure>
				{% if work.external_url %}
				<a href="{{ work.external_url }}">
				{% else %}
				<a href="{{ work.url }}">
				{% endif %}
				<img src="{{ work.image }}" />
				</a>
			</figure>
			{% endif %}
		</article>
		{% endfor %}
	</section>
</section>
