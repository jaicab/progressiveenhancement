---
layout: listing
title: Examples
---

<ul class="l-resource-list">
{% assign itemlist = (site.resourceexample | sort: 'title') %}
{% for item in itemlist %}
<li class="c-resource">
	<a class="c-resource__link" href="{{ item.link }}">
		<h4 class="c-resource__title">{{ item.title }}</h4>

		{{ item.content }}
	
		By <strong>
		{{ item.author }}
		</strong>


		{% if item.site %}
			on <strong>{{ item.site }}</strong>
		{% endif %}
	</a>
</li>
{% endfor %}
</ul>