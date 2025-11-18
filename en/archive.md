---
layout: main-en
title: Blog Archive
---
# Blog Archive

<div class="category-filter">
  {% assign pragmatic = site.tags.en | where_exp: "post", "post.tags contains 'pragmatic-delivery-en'" %}
  {% assign leadership = site.tags.en | where_exp: "post", "post.tags contains 'leadership-en'" %}
  {% assign governance = site.tags.en | where_exp: "post", "post.tags contains 'governance-en'" %}
  {% assign consulting = site.tags.en | where_exp: "post", "post.tags contains 'consulting-en'" %}
  {% assign ai = site.tags.en | where_exp: "post", "post.tags contains 'ai-en'" %}
  {% assign team = site.tags.en | where_exp: "post", "post.tags contains 'team-culture-en'" %}
  {% assign cicd = site.tags.en | where_exp: "post", "post.tags contains 'ci-cd-en'" %}
  {% assign infra = site.tags.en | where_exp: "post", "post.tags contains 'infrastructure-en'" %}
  <span class="category-tag" data-category="all" onclick="filterPosts('all')"><strong>All</strong> <span>({{ site.tags.en.size }})</span></span>
  <span class="category-tag" data-category="pragmatic-delivery-en" onclick="filterPosts('pragmatic-delivery-en')"><strong>Pragmatic Delivery</strong> <span>({{ pragmatic.size }})</span></span>
  <span class="category-tag" data-category="leadership-en" onclick="filterPosts('leadership-en')"><strong>Leadership</strong> <span>({{ leadership.size }})</span></span>
  <span class="category-tag" data-category="governance-en" onclick="filterPosts('governance-en')"><strong>Governance</strong> <span>({{ governance.size }})</span></span>
  <span class="category-tag" data-category="consulting-en" onclick="filterPosts('consulting-en')"><strong>Consulting</strong> <span>({{ consulting.size }})</span></span>
  <span class="category-tag" data-category="ai-en" onclick="filterPosts('ai-en')"><strong>AI & Automation</strong> <span>({{ ai.size }})</span></span>
  <span class="category-tag" data-category="team-culture-en" onclick="filterPosts('team-culture-en')"><strong>Team Culture</strong> <span>({{ team.size }})</span></span>
  <span class="category-tag" data-category="ci-cd-en" onclick="filterPosts('ci-cd-en')"><strong>CI/CD</strong> <span>({{ cicd.size }})</span></span>
  <span class="category-tag" data-category="infrastructure-en" onclick="filterPosts('infrastructure-en')"><strong>Infrastructure</strong> <span>({{ infra.size }})</span></span>
</div>

## All Posts
<ul class="posts">
	{% assign sorted_posts = site.tags.en | sort: 'date' | reverse %}
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
