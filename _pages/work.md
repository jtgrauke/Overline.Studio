---
layout: default
title: Work
description: Overline is a design studio. We work with growing tech-companies to raise their perceived value through brand identity and web design. Through our collaborative process, we design a presence that attracts the right customers, top-talent, and investors, so you can bring your brand to life.
featured_image: '/images/social.jpg'
---


<section>
	<div class="wrap mt5">
		<div class="portfolio span-12 ">
			{% assign sorted_projects = site.projects | sort: 'date' | reverse %}
			{% for project in sorted_projects %}
			<div class="portfolio-item">
				<a class="portfolio-item__link" href="{{ project.url | relative_url }}">
					<div class="portfolio-item__image">
						<img src="{{ project.featured_image | relative_url }}" alt="{{ project.title }}">
					</div>
					<div class="portfolio-item__content">
						<h2 class="portfolio-item__title displayMedium">{{ project.title }}</h2>
						<h3 class="portfolio-item__subtitle displayMedium">{{ project.description }}</h3>
						<p class="portfolio-item__services caption">{{ project.services }}</p>
					</div>
				</a>
			</div>
			{% endfor %}
		</div>
	</div>
</section>