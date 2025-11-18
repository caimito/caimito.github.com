---
layout: main-de
title: Notizblog Archiv
---
# Notizblog Archiv

## Alle Beiträge
<ul class="posts">
	{% assign sorted_posts = site.tags.de | sort: 'date' | reverse %}
	{% for post in sorted_posts %}
	<li>{{ post.date | date: "%d.%m.%Y" }} - <a href="{{ post.url }}">{{ post.title }}</a></li>
	{% endfor %}
</ul>