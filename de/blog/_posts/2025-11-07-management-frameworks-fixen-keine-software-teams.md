---
layout: blog-de
title: Management-Frameworks reparieren keine Software-Teams — Software-Entwicklung schon
tags:
- de
- sns-de
- dev-advocate-de
---
<p>{{ page.date | date: "%d.%m.%Y" }}, <em>Von Stephan Schwab</em></p>

Alle paar Jahre verspricht ein neues Management-Framework Erlösung.
Es kommt mit Canvas, Rollen, Zeremonien und farbcodierten Haftnotizen. Es behauptet „Verschwendung“, „Engpässe“ und „Fehlausrichtung“ aufzudecken.
Und fair genug — oft zeigt es tatsächlich etwas.
Aber was danach passiert, ist meist der Punkt an dem es schiefgeht.

## Frameworks sehen Symptome — Software-Entwicklung beseitigt Ursachen

Ein Framework ist diagnostisch, nicht heilend.
Es kann zeigen, dass Kommunikation kaputt ist, dass angefangene Arbeit sich stapelt oder dass Releases ständig fehlschlagen. Aber nichts davon lässt sich mit noch mehr Frameworks, Ritualen oder Führungsparolen beheben.
Diese Probleme sitzen tief in Code, Werkzeugkette und technischen Gewohnheiten.

Schlechte Commits erzeugen Integrationshölle — nicht schlechte Standups.
Unzuverlässige Releases kommen von fehlenden Tests — nicht von fehlenden Retros.
Lange Durchlaufzeiten entstehen durch schwaches CI/CD — nicht durch schwache Sprint-Planung.

Solange grundlegende Praktiken der Software-Entwicklung sich nicht ändern — Versionskontroll-Disziplin, Automatisierung, Testabdeckung, Modularität — wird keine Methodentheater-Vorstellung die Lieferung glattziehen.

## Der Reflex des Beraters: „Wir müssen die Entwickler reparieren“

Viele Management-Berater, oft mit wenig oder keiner Programmiererfahrung, sehen Entwickler als Blackbox, die kalibriert werden muss.
Sie glauben, das Problem sei „Entwickler-Mindset“ oder „Kultur“.
Dann führen sie Rituale ein um „Zusammenarbeit zu verbessern“ — als wäre die Hauptursache emotional statt technisch.

Aber Software ist keine Psychologie. Sie ist ein System aus Logik, Feedback und Constraints.
Wenn Entwickler beliebige Frameworks ablehnen, dann nicht aus Starrsinn — sondern weil sie bereits in einer Domäne mit hartem Feedback arbeiten: Code kompiliert oder nicht, Tests bestehen oder fallen durch, Nutzer bleiben oder springen ab.
In diesem Umfeld zählt Wahrheit mehr als Theater.

## Die echte Lösung: Hygiene der Software-Entwicklung

Wer Lieferung wirklich verbessern will, beginnt bei Dingen die Feedback schneller und Fehler günstiger machen:

<table>
<thead>
<tr><th>Bereich</th><th>Echte Abhilfe</th><th>Management-Äquivalent (Symptom)</th></tr>
</thead>
<tbody>
<tr><td>Testing</td><td>Automatisierte Tests + CI/CD</td><td>„Quality Circle“ oder „QA Ownership Workshop“</td></tr>
<tr><td>Architektur</td><td>Klare modulare Grenzen</td><td>„Abhängigkeiten zwischen Teams reduzieren“</td></tr>
<tr><td>Release</td><td>Kleine, reversible Änderungen</td><td>„Risiko senken durch mehr Freigaben“</td></tr>
<tr><td>Kommunikation</td><td>Gemeinsame Code-Sichtbarkeit</td><td>„Cross‑funktionales Alignment Meeting“</td></tr>
</tbody>
</table>

Frameworks zeigen Schmerzen — Software-Entwickler entfernen Ursachen.
Das ist der fundamentale Unterschied.

## Lasst Software-Entwickler ihre Arbeit gestalten

Jedes ernsthafte Handwerk hat seine innere Logik.
Man sagt einem Chirurgen nicht, wie er das Skalpell hält, oder einer Pilotin wie sie Turbulenzen handhabt. Man vertraut ihrem Urteil, weil man ihrer Ausbildung vertraut.

Software-Entwicklung ist nicht anders.
Wenn Außenstehende vorschreiben wie Software-Entwickler planen, schätzen oder „sich selbst organisieren“ sollen, befähigen sie sie nicht — sie unterbrechen Fluss.

Gutes Management „repariert“ keine Software-Entwickler.
Es schafft Bedingungen, damit sie das System reparieren.

## Die harte Wahrheit

Kein Framework — egal wie elegant — wird je einen Test schreiben, ein Legacy-Modul refaktorisieren oder eine fehlschlagende Pipeline debuggen.
Das ist Arbeit für Software-Entwickler — nicht für Berater.

Wenn ein Management-Framework hilft Verschwendung zu sehen: gut. Nutze es als Spiegel.
Aber sobald gehandelt werden muss, gib den Spiegel den Menschen, die das Produkt wirklich bauen.

Sie müssen nicht „repariert“ werden.
Sie brauchen Raum, Werkzeuge und Vertrauen ihre Arbeit zu tun.

## TL;DR

Frameworks zeigen Dysfunktion.
Software-Entwicklung behebt sie.
Berater, die versuchen „Entwickler zu reparieren“, lösen das falsche Problem.
