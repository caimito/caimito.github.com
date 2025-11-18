# Copilot Instructions

Authoritative directives for AI assistance (GitHub Copilot, chat, or other agents) working in this repository.

## Core Principles
1. Preserve intent and voice of existing content (author: Stephan Schwab).
2. Prefer minimal, precise edits over wholesale rewrites.
3. Never add cross-language link paragraphs inside blog posts.
4. Use repository conventions; infer when unspecified and document assumptions via HTML comments.

## Blogging Conventions
| Aspect | English | German | Spanish |
|--------|---------|--------|---------|
| Layout | `blog-en` | `blog-de` | `blog-es` |
| Author line | `By Stephan Schwab` | `Von Stephan Schwab` | `Por Stephan Schwab` |
| Tags (minimum) | `en`, `sns-en`, `dev-advocate-en` | `de`, `sns-de`, `dev-advocate-de` | `es`, `sns-es`, `dev-advocate-es` |
| Date display | `{{ page.date | date: "%d.%m.%Y" }}` across all languages |

### Blog Post Category Tags (Required)
**Each blog post must include appropriate category tags in addition to the minimum required tags (language, author, role).**

**Available category tags (use existing tags only, do not create new ones):**

**Priority 1 - Most Common:**
- **Pragmatic Delivery**: `pragmatic-delivery-en` / `pragmatische-auslieferung-de` / `entrega-pragmatica-es`
  - Articles about smart software delivery, process critique, methodology independence
- **Leadership**: `leadership-en` / `fuehrung-de` / `liderazgo-es`
  - Organizational change, executive decision-making, CTO challenges
- **Governance**: `governance-en` / `fuehrung-de` / `gobernanza-es`
  - Visibility, metrics, governing without control

**Priority 2 - Secondary:**
- **Consulting**: `consulting-en` / `beratung-de` / `consultoria-es`
  - Consultant-developer relationships, boundaries, collaboration
- **AI & Automation**: `ai-en` / `ki-de` / `ia-es`
  - AI impact on software, automation, future of work
- **Team Culture**: `team-culture-en` / `teamkultur-de` / `cultura-de-equipo-es`
  - Team dynamics, collaboration, effectiveness

**Priority 3 - Technical:**
- **CI/CD**: `ci-cd-en` / `ci-cd-de` / `ci-cd-es`
  - Continuous integration, DevOps, deployment pipelines
- **Infrastructure**: `infrastructure-en` / `infrastruktur-de` / `infraestructura-es`
  - Cloud, infrastructure decisions, cost optimization

**Tagging guidelines:**
- Add 1-3 category tags per post based on primary themes
- Choose tags that best represent the article's core message
- When a post covers multiple topics, prioritize the main theme

### New Blog Post Formatting
When preparing new blog content for publication:
1. **Heading hierarchy**: The `title` in the YAML front matter becomes the page's H1 (level 1 heading). The subheading immediately after (within `article-intro` or standalone) should be H2 (level 2, `##`). All subsequent section headings in the article body are H2 (level 2, `##`), with subsections as H3 (level 3, `###`) and deeper as needed. Never use H1 (`#`) within the article body.
2. **Add introduction section** with:
   - A subheading (level 2 heading, `##`) that summarizes the article's theme
   - Wrap entire introduction in `<div class="article-intro">` with closing `</div>`
   - Date and author line: `<p>{{ page.date | date: "%d.%m.%Y" }}, <em>By Stephan Schwab</em></p>` (or `Von` for German, `Por` for Spanish)
   - Gravatar image linked to about page: `<a href="/en/about.html"><img src="https://gravatar.com/avatar/663d11426b0a187ddac59f8c17ce61b4?s=120&d=robohash&r=x" class="avatar" /></a>` (adjust language path: `/de/about.html` or `/es/about.html`)
   - Summary paragraph wrapped in `<p>` tags describing the article's key points and themes
3. **Remove horizontal rules (`---`)** between sections within the article body (keep only in YAML front matter)
4. **Blog post cadence**: New blog posts must be dated at least 3 days after the previous post. Check the most recent post date in each language's `blog/_posts/` directory and ensure the new post date is at minimum 3 days later. Do not publish posts more frequently than every 3 days.
5. **Target length**: Initial blog posts should be between 700 and 1,800 words. This provides sufficient depth without becoming overwhelming. Longer pieces (2,000+ words) should be reserved for comprehensive guides or when the topic genuinely requires extended treatment.

### Navigation / Menu
* Treat English `menu-en.html` as canonical for structure and ordering.
* Other language menus mirror items present (omit any English commented out TODO items unless explicitly enabled in English first).
* Ensure each link points to its language-specific path (e.g. `/es/consulting.html` not root version).
* When a translated target is updated (placeholder removed), verify the menu link still matches the generated output filename.
* Do not introduce cross-language links inside menus; language switching is handled by flag icons.

Front matter example:
```yaml
---
layout: blog-en
title: "Example Title"
excerpt: "A 1-3 sentence summary of the article that captures its key insights and themes. This appears in RSS feeds, social media previews, and Buffer. Extract from the summary paragraph inside article-intro, excluding date/author/avatar."
tags:
  - en
  - sns-en
  - dev-advocate-en
---
```

### Blog Post Excerpts (Required)
**All blog posts must include an `excerpt:` field in the front matter.**
- Extract the text from the summary paragraph within the `<div class="article-intro">` section
- Exclude date, author line, and avatar image—include only the summary paragraph text
- Length: 1-3 sentences (typically 150-250 words) capturing the article's core themes and insights
- Purpose: Appears in RSS feeds (`posts.xml`), social media previews, Buffer scheduling, and any content aggregation systems
- When creating new posts: Write the excerpt first to clarify the article's message, then expand in the intro section
- When translating posts: Translate the excerpt along with the title and content

## Translation Rules
* Mirror section headings and ordering from source language.
* Adapt idioms; do not translate product names or code identifiers.
* Maintain bullet lists, tables, code blocks verbatim except for prose.
* If a TL;DR exists in original, translate it; do not add new TL;DR.
* Do not insert cross-language links. Instead leave a silent HTML comment:
  `<!-- Cross-language links intentionally omitted -->`

### German Language Style (Executive Audience)
* Use standard business German; avoid colloquialisms.
* Do **not** gender: use generic forms like "Entwickler", "Kunde", "Nutzer". Do not use Binnen-I, slashes, colons, asterisks, or parentheses (e.g. no "Entwickler:innen", "Kund*innen", "Entwickler/-innen").
* Prefer concise sentences; emphasize clarity and decision-relevant insight.
* Avoid culture-war or linguistic debates; keep focus on content value.
* If a source English text uses a gender-neutral concept, translate with the established generic form (e.g. "developer" -> "Entwickler").
* Avoid literal translations of strong English metaphors (e.g. "kills Agile"). Use neutral business German alternatives like "schafft nicht ab", "beendet", "macht obsolet", depending on nuance.
* Avoid unnecessary English nouns (e.g. "Engineering") in German content. Prefer "Software-Entwicklung", "technische Umsetzung", or context-appropriate business terms (e.g. "Produktentwicklung") and use "fachlicher Experte" instead of "Domänenexperte" when describing domain specialists.
* Avoid "germanized" English verbs (e.g. "reviewt", "deployt", "gemerged"). Use standard German equivalents: "prüfen", "ausliefern", "verteilen", "zusammenführen". If no concise equivalent exists, rephrase (e.g. describe the action: "Code wird überprüft und anschließend ausgeliefert").
* Translate "governance" as "Führung" (leadership/guidance), not "Steuerung" (control/steering). This preserves the conceptual distinction between governance (systematic guidance through instrumentation) and control (direct oversight).

## Glossary
<!-- Added initial multilingual glossary. Assumptions: retaining existing tag names (e.g. dev-advocate-*) for backward compatibility; proposing preferred prose alternatives. -->

| English Term | German Preferred | Spanish Preferred | Notes |
|--------------|------------------|-------------------|-------|
| advocate (Developer Advocate) | (prose) "Ansprechpartner für Entwickler" / role label: "Developer Advocate" (kept English) | "evangelista de desarrolladores" (or "promotor técnico") | German: Avoid literal "Advokat" or awkward calques; use descriptive phrase. Emphasize it's a praxisnaher Senior-Software-Entwickler (schreibt produktiven Code, eingebettet im Team) – nicht nur Kommunikation oder Schulung. Tag `dev-advocate-de` retained for consistency. |
| additional hires | "weitere Mitarbeiter" | "contrataciones adicionales" | Use people-focused wording, not "zusätzliche Stellen" (positions) when emphasizing added team members. |
| governance | Führung | gobernanza | Maintain distinction vs. control (Steuerung / control). |
| domain expert | fachlicher Experte | experto funcional | Avoid "Domänenexperte"; Spanish: choose functional/business context term. |
| developer | Entwickler | desarrollador | Generic, non-gendered forms. |
| to deploy (software) | ausliefern / verteilen | desplegar | Choose based on context: ausliefern (release), verteilen (distribution). |
| to merge (code) | zusammenführen | fusionar | Describe action instead of anglicisms ("mergen"). |
| release | Veröffentlichung | lanzamiento | German: also "Release" sometimes used; prefer "Veröffentlichung" in formal text. |
| layout | Layout | diseño | Keep English in technical repo contexts; Spanish translate as "diseño" when referring to page structure. |
| introduction section | Einleitung | introducción | For blog intro wrapped in `div.article-intro`. |
| summary (article) | Zusammenfassung | resumen | Keep concise; may appear in intro paragraph. |
| gender-neutral generic (developer, user) | generische Form (z.B. "Entwickler", "Nutzer") | forma genérica ("desarrollador", "usuario") | German: no gender markers; Spanish typically default masculine generic. |
| engineering (software context) | Software-Entwicklung / Entwicklung | ingeniería de software / desarrollo de software | In German, "Engineering" evokes Maschinen-/Bauingenieurwesen; prefer explicit Software-Entwicklung to avoid Missverständnisse. |
| methodology reseller | Methoden-Verkäufer | revendedor de metodologías | Prefer concise "Methoden-Verkäufer"; avoid calque "Methodik-Wiederverkäufer" which sounds awkward. Emphasize hands-on delivery over packaged frameworks. |
| runtime signal | Laufzeit-Signal / Laufzeitdaten (kontextabhängig) | señal de ejecución / telemetría en tiempo de ejecución | German: Prefer "Laufzeitdaten" for plural evidence, use "Laufzeit-Signal" when emphasizing single metric; avoid generic "Runtime" anglicism. |
| usage data | Nutzungsdaten | datos de uso | Distinguish from Meinungen; emphasizes echte Interaktionen produktiver Nutzer. |
| repeatable innovation system | wiederholbares Innovations‑System | sistema repetible de innovación | Avoid marketing flourish; keep hyphenated compound in German for clarity; describes flow + integration + evidence loop. |
| production deployment | Produktiv-Auslieferung / Produktionsbereitstellung | despliegue a producción | German: Prefer "Produktiv-Auslieferung" (delivery act) or "Produktionsbereitstellung" (readiness) depending on emphasis; avoid Anglizismus "Production Deployment". |
| safe merge (code) | sichere Zusammenführung | fusión segura | Emphasize outcome (risikoarm integrierter Code) rather than tool brand or branching model. |
| delivery flow | Lieferfluss | flujo de entrega | Describes progression of validierte Arbeit through Entwicklung to produktive Nutzung; avoid vague "Prozess". |
| deployment frequency | Auslieferungsfrequenz | frecuencia de despliegue | Use when emphasizing rhythm of small, risikoarme Produktiv-Auslieferungen; avoid Anglizismus "Deployment Frequency" in German prose. |
| Statement of Work (SOW) | Leistungsvereinbarung | declaración de trabajo (SOW) | Use "Leistungsvereinbarung" in German prose; avoid leaving "SOW" untranslated except optionally in first mention for clarity. Focus on Problem, Outcomes, Mess-Signale, Randbedingungen. |
| delivery (noun, software context) | Auslieferung | entrega | Prefer "Auslieferung" for the act/result; distinguish from "Lieferung" (generic shipping). Use in compounds (Auslieferungsfrequenz, Produktiv-Auslieferung). |
| product organizations | Software-Anbieter | organizaciones de producto | German: Prefer "Software-Anbieter" to emphasize provider role over internal structure; avoid generic "Produktorganisationen". |
| integration friction | Integrations-Reibung | fricción de integración | Describes hindered Flow durch aufgestaute Integrationsarbeit; keep hyphenation consistent (Integrations-Reibung) for readability. |
| defect rate | Fehlerrate | tasa de defectos | Overall proportion of Fehler; distinct from Durchrutschrate (Defect Escape Rate). Use Fehlerrate for aggregate quality discussion. |
| defect escape rate | ausgelieferte Fehler (Rate ausgelieferter Fehler) | tasa de escape de defectos | Rate at which Fehler erst in späteren Stufen (z.B. Produktion) sichtbar werden; avoid leaving only English metric name. |
| user adoption | Nutzerakzeptanz | adopción de usuarios | Emphasizes real produktive Nutzung vs Meinungen. Avoid metaphorical "traction" in German. |
| production readiness | Produktionsbereitschaft | preparación para producción | State prior to Produktiv-Auslieferung; distinct from Deployment act. |
| management framework | Management-Framework | marco de gestión | Generic framework (Skalierung, Governance); avoid over-translation; keep hyphen. |
| embedded advocacy | Embedded Advocacy (eingebettete technische Unterstützung) | advocacy integrada | Role label kept English; German prose clarifies technische, hands-on Unterstützung im Team. |
| executive coaching | Executive-Coaching | coaching ejecutivo | Focus on faktenbasierte Entscheidungsfähigkeit via direkte Einblicke (Pipelines, Telemetrie). |
| validated user insight | validierte Erkenntnis zum Nutzererlebnis | insight validado sobre la experiencia de usuario | Evidence-based qualitative + quantitative Nutzerbeobachtung (Nutzungsdaten + Verhalten) verdichtet zu umsetzbarer Erkenntnis; avoid vague 'Feedback'. |
| delivered software (result) | ausgelieferte Software | software entregada | Concrete result of a Produktiv-Auslieferung; use when emphasizing software now in produktiver Nutzung (avoid generic 'bereitgestellte Lösung'). |

<!-- Future additions: SEO terms, build workflow vocabulary. -->

## Prohibited Actions
* No insertion of marketing fluff, self-promotion, or unrelated external links.
* No exposure of secrets (webhook URLs, tokens). Use `${{ secrets.MATTERMOST_WEBHOOK }}` only in workflows.
* No alteration of the scheduled build workflow unless explicitly tasked.

## Workflows
* Scheduled build/deploy: `.github/workflows/scheduled-pages-build.yml` — retains notification steps. When editing, ensure start, build result, and deploy notifications survive unless asked to remove.

## Commit Guidance
* Group related translation files in a single commit when feasible.
* For minor copy edits, commit per file to keep history granular.
* Commit message format suggestions:
  * `feat(blog-de): add German translation for <slug>`
  * `fix(blog-es): correct accent in title`.

## Validation Checklist (AI must self-check)
1. Correct layout per language.
2. Tags include required language markers.
3. No cross-language links inserted.
4. Build workflow untouched (unless mandated).
5. Markdown lints (no stray backticks, unmatched HTML tags).

## Future Considerations (Do Not Implement Yet)
* Global hreflang tags (may move to layout).
* Automated multi-language navigation.

## Security
* Secrets only via GitHub Actions `${{ secrets.* }}` expressions.
* Never store secret values in repository files.
