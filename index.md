---
layout: full-width
title: Taylor McKnight
description: I started and lead the design team at Industry Dive, a high-growth business journalism publisher in Washington, DC
og_title: Taylor McKnight
og_description: I started and lead the design team at Industry Dive, a high-growth business journalism publisher in Washington, DC
og_image: /media/img/about/mcknight_headshot.jpg
og_type: website
---
<section class="" style="margin-top:20vh;">
	<section class="grid page-header">
		<div class="full-width">
			<h1>{{ page.title }}
			</h1>
			<p>VP of Design at <a href="https://www.industrydive.com/">Industry Dive</a>. View the design department's work at <a href="https://industrydive.design/">IndustryDive.design</a></p>
			<p>Learn more <a href="{{ site.url }}/about">about McKnight</a>.</p>
		</div>
	</section>
</section>
<!--
<section class="grid">
	<div class="full-width">
	</div>
</section>

<!--
<section class="stripe-section-2">
	<section class="grid sub-section-header">
		<div class="full-width">
			<h2>Space</h2>
		</div>
	</section>
	
</section>

<section class="stripe-section-2">
	<section class="grid sub-section-header">
		<div class="full-width">
			<h2>Journalism</h2>
		</div>
	</section>
	<section class="grid-wrapper tiles">
		{% assign journalismprojects = site.projects | where: "category", "journalism" | sort:"weight" %}
		{% for page in journalismprojects %}
		<article>
			<figure>
				{% if page.image %}
				{% if page.external_url %}
				<a href="{{ page.external_url }}">
				{% else %}
				<a href="{{ page.url }}">
				{% endif %}
				<img src="{{ page.image }}" />
				</a>
				{% endif %}
				<figcaption>
					{% if page.external_url %}
					<a href="{{ page.external_url }}">
					{% else %}
					<a href="{{ page.url }}">
					{% endif %}
					{% if page.label %}
					<p class="label">{{ page.label }}</p>
					{% endif %}
					<h3>
						{{ page.title }}
					</h3>
					</a>
					<p>
					{{ page.description }}
					</p>
					<p>
					{% if page.external_url %}
					<a href="{{ page.external_url }}">
					{% else %}
					<a href="{{ page.url }}">
					Read more
					{% endif %}
					</a>
					</p>
				</figcaption>
			</figure>
		</article>
		{% endfor %}
	</section>


</section>-->