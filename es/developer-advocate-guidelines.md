---
layout: main-es
title: Senior Developer Advocate Guía
---
<div class="two-columns">
  <div>
    {% capture left_column %}{% include_relative dev-advocate-guidelines.md %}{% endcapture %}
    {{ left_column | markdownify }}
  </div>
  <div class="sidebar reference-projects">
  <p>El <strong>Senior Developer Advocate</strong> conecta la intención estratégica con la realidad de ingeniería. Operamos con neutralidad de método: sin promover frameworks de marca ni debatir etiquetas — solo mejoras prácticas que vuelven ejecutable la estrategia. Al involucrar liderazgo e ingeniería, dirección, decisiones y entrega se mantienen alineadas y basadas en hechos.</p>

    <h2>Informes de la Práctica</h2>
    <ul class="posts">
      {% for post in site.tags.dev-advocate-es limit:10 %}
      <li><a href="{{ post.url }}">{{ post.title }}</a> ({{ post.date | date: "%d.%m.%Y" }})</li>
      {% endfor %}
    </ul>

    {% capture right_column %}{% include_relative dev-advocate-references.md %}{% endcapture %}
    {{ right_column | markdownify }}
  </div>
</div>
