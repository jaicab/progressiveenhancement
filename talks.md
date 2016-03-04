---
layout: listing
title: Talks
---

<ul class="l-resource-list">
{% assign itemlist = (site.resourcetalk | sort: 'title') %}
{% for item in itemlist %}
<li class="c-resource">
	<a class="c-resource__link" href="{{ item.link }}">
		<h4 class="c-resource__title">{{ item.title }}</h4>

		{{ item.content }}
	
	
		By <strong>
			{{ item.speaker }}
		</strong>


		{% if item.conference %}
			at <strong>{{ item.conference }}</strong>
		{% endif %}
	</a>
</li>
{% endfor %}
</ul>