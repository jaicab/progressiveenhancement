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
		{% if item.site %}
			<a href="{{ item.site }}">{{ item.author }}</a>
		{% else %}
			{{ item.author }}
		{% endif %}
		</strong>


		{% if item.site %}
			on <strong>{{ item.site }}</strong>
		{% endif %}
	</a>
</li>
{% endfor %}
</ul>