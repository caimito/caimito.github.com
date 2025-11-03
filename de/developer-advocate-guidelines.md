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
    <p>Der <strong>Senior Developer Advocate</strong> verbindet Management-Vision mit technischer Realität. Wir arbeiten neben agilen, Lean- oder OKR-Initiativen – und verwandeln Strategie in nachhaltige Ausführung ohne Reibung oder Konkurrenz. Durch die Ansprache sowohl von Vorstandsebene als auch Entwicklungsteams bleiben Richtung, Entscheidungen und Lieferung ausgerichtet.</p>

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
