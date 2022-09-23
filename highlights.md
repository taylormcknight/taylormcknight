---
layout: full-width
title: Career Highlights
description: Highlights from 2012-22
og_title: Career Highlights
og_description:  Career Highlights
og_image: /media/img/about/headshot-2022.jpg
og_type: website
---
<section class="grid page-header">
	<div class="full-width">
		<h1>{{ page.title }}</h1>
		<p>Accomplishments of teams I've created and led</p>
	</div>
</section>
<section class="stripe-section-2">
	<section class="grid-wrapper feed">
		{% for highlights in site.categories.highlights %}
		<article>
			<figcaption>
				{% if highlights.external_url %}
				<a href="{{ highlights.external_url }}">
				{% else %}
				<a href="{{ highlights.url }}">
				{% endif %}
				<h3>
					{{ highlights.title }}
				</h3>
				</a>
				<p class="label">{{ highlights.date | date: "%-d %B %Y" }}</p>
				<p class="description">{{ highlights.description }}</p>
				<p>
				{% if highlights.external_url %}
				<a href="{{ highlights.external_url }}">
				{% else %}
				<a href="{{ highlights.url }}">
				{% endif %}
				Read more
				</a>
				</p>
			</figcaption>
			{% if highlights.image %}
			<figure>
				{% if highlights.external_url %}
				<a href="{{ highlights.external_url }}">
				{% else %}
				<a href="{{ highlights.url }}">
				{% endif %}
				<img src="{{ highlights.image }}" />
				</a>
			</figure>
			{% endif %}
		</article>
		{% endfor %}
	</section>
</section>
