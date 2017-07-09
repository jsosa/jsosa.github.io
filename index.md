---
#
# You don't need to edit this file, it's empty on purpose.
# Edit minima's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
#
layout: default
---

cover page

{% if site.posts.size == 0 %}
	<p class="text-center">Nothing published yet!</p>
{% elsif site.paginate %}
	{% for post in paginator.posts %}
		{% if post.category == 'blog' %}
			{% if post.hidden != true %}
				{% include blog-post.html %}
			{% endif %}
		{% endif %}
	{% endfor %}

	{% include pagination.html%}
{% else %}
	{% for post in site.posts %}
		{% if post.category == 'blog' %}
			{% if post.hidden != true %}
				{% include blog-post.html %}
			{% endif %}
		{% endif %}
	{% endfor %}
{% endif %}