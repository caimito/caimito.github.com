---
layout: main-de
title: Senior Developer Advocate Leitfaden
---
<div class="two-columns">
  <div>
    {% capture left_column %}{% include_relative dev-advocate-guidelines.md %}{% endcapture %}
    {{ left_column | markdownify }}
  </div>
  <div class="sidebar reference-projects">
  <p>Der <strong>Senior Developer Advocate</strong> verbindet Management-Absicht mit technischer Realität. Methodenneutral – keine Förderung von Marken-Frameworks oder Label-Debatten, sondern praktische Verbesserungen, die Strategie ausführbar machen. Durch die Ansprache von Führung und Engineering bleiben Richtung, Entscheidungen und Lieferung faktenbasiert und ausgerichtet.</p>

    <h2>Berichte aus der Praxis</h2>
    <ul class="posts">
      {% for post in site.tags.dev-advocate-de limit:10 %}
      <li><a href="{{ post.url }}">{{ post.title }}</a> ({{ post.date | date: "%d.%m.%Y" }})</li>
      {% endfor %}
    </ul>

    {% capture right_column %}{% include_relative dev-advocate-references.md %}{% endcapture %}
    {{ right_column | markdownify }}
  </div>
</div>
