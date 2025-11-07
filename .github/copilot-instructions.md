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
tags:
  - en
  - sns-en
  - dev-advocate-en
---
```

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
