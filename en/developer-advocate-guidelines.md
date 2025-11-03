---
layout: main-en
title: Working Successfully with a Senior Developer Advocate
---
<div class="two-columns">
  <div>
    {% capture left_column %}{% include_relative dev-advocate-guidelines.md %}{% endcapture %}
    {{ left_column | markdownify }}
  </div>
  <div class="sidebar reference-projects">
    <p>The <strong>Senior Developer Advocate</strong> connects management vision with engineering reality.  
    We work seamlessly alongside Agile, Lean, or OKR initiatives — turning strategy into sustainable execution without creating friction or competition.  
    By engaging both the boardroom and the development team, we ensure that direction, decisions, and delivery stay perfectly aligned.</p>

    <h2>Reports from Practice</h2>
    <ul class="posts">
      {% for post in site.tags.dev-advocate-en limit:10 %}
      <li><a href="{{ post.url }}">{{ post.title }}</a> ({{ post.date | date: "%d.%m.%Y" }})</li>
      {% endfor %}
    </ul>

    {% capture right_column %}{% include_relative dev-advocate-references.md %}{% endcapture %}
    {{ right_column | markdownify }}
  </div>
</div>