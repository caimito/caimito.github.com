---
layout: main-es
title: Archivo del Blog
---
# Archivo del Blog

## Todas las Entradas
<ul class="posts">
	{% assign sorted_posts = site.tags.es | sort: 'date' | reverse %}
	{% for post in sorted_posts %}
	<li>{{ post.date | date: "%d.%m.%Y" }} - <a href="{{ post.url }}">{{ post.title }}</a></li>
	{% endfor %}
</ul>
