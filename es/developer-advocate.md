---
layout: main-es
title:
---
<div class="two-columns">
	<div>
		{% capture left_column %}{% include_relative dev-advocate-body.md %}{% endcapture %}
		{{ left_column | markdownify }}
	</div>
	<div class="sidebar reference-projects">
		<p>El <strong>Senior Developer Advocate</strong> conecta la visión de gestión con la realidad de ingeniería. Operamos con neutralidad de método: ninguna etiqueta, marco o estilo es requisito para colaborar. Convertimos estrategia en ejecución sostenible mediante ingeniería práctica y mejoras visibles de flujo, calidad y claridad. Al involucrar tanto a la dirección como al equipo de desarrollo mantenemos alineadas orientación, decisiones y entrega sin fricción por debates metodológicos.</p>

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
