---
layout: main-es
title: Archivo del Blog
---
# Archivo del Blog

<div class="category-filter">
  {% assign pragmatic = site.tags.es | where_exp: "post", "post.tags contains 'entrega-pragmatica-es'" %}
  {% assign leadership = site.tags.es | where_exp: "post", "post.tags contains 'liderazgo-es'" %}
  {% assign governance = site.tags.es | where_exp: "post", "post.tags contains 'gobernanza-es'" %}
  {% assign consulting = site.tags.es | where_exp: "post", "post.tags contains 'consultoria-es'" %}
  {% assign ai = site.tags.es | where_exp: "post", "post.tags contains 'ia-es'" %}
  {% assign team = site.tags.es | where_exp: "post", "post.tags contains 'cultura-de-equipo-es'" %}
  {% assign cicd = site.tags.es | where_exp: "post", "post.tags contains 'ci-cd-es'" %}
  {% assign infra = site.tags.es | where_exp: "post", "post.tags contains 'infraestructura-es'" %}
  <span class="category-tag" data-category="all" onclick="filterPosts('all')"><strong>Todas</strong> <span>({{ site.tags.es.size }})</span></span>
  <span class="category-tag" data-category="entrega-pragmatica-es" onclick="filterPosts('entrega-pragmatica-es')"><strong>Entrega Pragmática</strong> <span>({{ pragmatic.size }})</span></span>
  <span class="category-tag" data-category="liderazgo-es" onclick="filterPosts('liderazgo-es')"><strong>Liderazgo</strong> <span>({{ leadership.size }})</span></span>
  <span class="category-tag" data-category="gobernanza-es" onclick="filterPosts('gobernanza-es')"><strong>Gobernanza</strong> <span>({{ governance.size }})</span></span>
  <span class="category-tag" data-category="consultoria-es" onclick="filterPosts('consultoria-es')"><strong>Consultoría</strong> <span>({{ consulting.size }})</span></span>
  <span class="category-tag" data-category="ia-es" onclick="filterPosts('ia-es')"><strong>IA y Automatización</strong> <span>({{ ai.size }})</span></span>
  <span class="category-tag" data-category="cultura-de-equipo-es" onclick="filterPosts('cultura-de-equipo-es')"><strong>Cultura de Equipo</strong> <span>({{ team.size }})</span></span>
  <span class="category-tag" data-category="ci-cd-es" onclick="filterPosts('ci-cd-es')"><strong>CI/CD</strong> <span>({{ cicd.size }})</span></span>
  <span class="category-tag" data-category="infraestructura-es" onclick="filterPosts('infraestructura-es')"><strong>Infraestructura</strong> <span>({{ infra.size }})</span></span>
</div>

## Todas las Entradas
<ul class="posts">
	{% assign sorted_posts = site.tags.es | sort: 'date' | reverse %}
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
