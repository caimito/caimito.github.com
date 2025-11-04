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
  <p>The <strong>Senior Developer Advocate</strong> connects management intent with engineering reality.  
  We operate method‑neutral: no promotion of branded frameworks or label debates — only practical improvements that make strategy executable.  
  By engaging both leadership and engineering, direction, decisions, and delivery remain fact‑based and aligned.</p>

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