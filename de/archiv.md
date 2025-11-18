---
layout: main-de
title: Notizblog Archiv
---
# Notizblog Archiv

<div class="category-filter">
  {% assign pragmatic = site.tags.de | where_exp: "post", "post.tags contains 'pragmatische-auslieferung-de'" %}
  {% assign leadership = site.tags.de | where_exp: "post", "post.tags contains 'fuehrung-de'" %}
  {% assign consulting = site.tags.de | where_exp: "post", "post.tags contains 'beratung-de'" %}
  {% assign ai = site.tags.de | where_exp: "post", "post.tags contains 'ki-de'" %}
  {% assign team = site.tags.de | where_exp: "post", "post.tags contains 'teamkultur-de'" %}
  {% assign cicd = site.tags.de | where_exp: "post", "post.tags contains 'ci-cd-de'" %}
  {% assign infra = site.tags.de | where_exp: "post", "post.tags contains 'infrastruktur-de'" %}
  <span class="category-tag" data-category="all" onclick="filterPosts('all')"><strong>Alle</strong> <span>({{ site.tags.de.size }})</span></span>
  <span class="category-tag" data-category="pragmatische-auslieferung-de" onclick="filterPosts('pragmatische-auslieferung-de')"><strong>Pragmatische Auslieferung</strong> <span>({{ pragmatic.size }})</span></span>
  <span class="category-tag" data-category="fuehrung-de" onclick="filterPosts('fuehrung-de')"><strong>Führung</strong> <span>({{ leadership.size }})</span></span>
  <span class="category-tag" data-category="beratung-de" onclick="filterPosts('beratung-de')"><strong>Beratung</strong> <span>({{ consulting.size }})</span></span>
  <span class="category-tag" data-category="ki-de" onclick="filterPosts('ki-de')"><strong>KI & Automatisierung</strong> <span>({{ ai.size }})</span></span>
  <span class="category-tag" data-category="teamkultur-de" onclick="filterPosts('teamkultur-de')"><strong>Teamkultur</strong> <span>({{ team.size }})</span></span>
  <span class="category-tag" data-category="ci-cd-de" onclick="filterPosts('ci-cd-de')"><strong>CI/CD</strong> <span>({{ cicd.size }})</span></span>
  <span class="category-tag" data-category="infrastruktur-de" onclick="filterPosts('infrastruktur-de')"><strong>Infrastruktur</strong> <span>({{ infra.size }})</span></span>
</div>

## Alle Beiträge
<ul class="posts">
	{% assign sorted_posts = site.tags.de | sort: 'date' | reverse %}
	{% for post in sorted_posts %}
	<li data-tags="{{ post.tags | join: ' ' }}">{{ post.date | date: "%d.%m.%Y" }} - <a href="{{ post.url }}">{{ post.title }}</a></li>
	{% endfor %}
</ul>

<script>
function filterPosts(category) {
  const posts = document.querySelectorAll('.posts li');
  const tags = document.querySelectorAll('.category-tag');
  
  // Update active state
  tags.forEach(tag => {
    if (tag.dataset.category === category) {
      tag.classList.add('active');
    } else {
      tag.classList.remove('active');
    }
  });
  
  // Filter posts
  posts.forEach(post => {
    if (category === 'all') {
      post.style.display = '';
    } else {
      const postTags = post.dataset.tags;
      post.style.display = postTags.includes(category) ? '' : 'none';
    }
  });
}

// Set 'All' as active on page load
document.addEventListener('DOMContentLoaded', function() {
  document.querySelector('.category-tag[data-category="all"]').classList.add('active');
});
</script>