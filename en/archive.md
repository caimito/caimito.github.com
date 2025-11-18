---
layout: main-en
title: Blog Archive
---
# Blog Archive

## All Posts
<ul class="posts">
	{% assign sorted_posts = site.tags.en | sort: 'date' | reverse %}
	{% for post in sorted_posts %}
	<li>{{ post.date | date: "%d.%m.%Y" }} - <a href="{{ post.url }}">{{ post.title }}</a></li>
	{% endfor %}
</ul>
