---
layout: blog-en
title: "How to Govern Without Control"
excerpt: "Leaders want both stability and innovation, but these forces pull in opposite directions. Many organizations reach for control—the illusion of safety through process, meetings, and metrics—yet in software, control rarely brings stability. It usually just slows feedback until systems fail silently. This article explores how governance differs from control: governance ensures the right things become visible at the right time through automated systems that tell the truth, not status reports. By replacing permission with visibility, technical leaders can manage feedback rather than people, creating sensor networks that surface misalignment early. Real stability looks noisy—with tests, builds, and human debate—but that noise is actually the sound of engineering excellence protecting the business from silent failure."
tags:
  - en
  - sns-en
  - dev-advocate-en
---
## Leadership Lessons from the Edge of Engineering Chaos

<div class="article-intro">
<p>{{ page.date | date: "%d.%m.%Y" }}, <em>By Stephan Schwab</em></p>

<a href="/en/about.html"><img src="https://gravatar.com/avatar/663d11426b0a187ddac59f8c17ce61b4?s=120&d=robohash&r=x" class="avatar" /></a>

<p>Leaders want both stability and innovation, but these forces pull in opposite directions. Many organizations reach for control—the illusion of safety through process, meetings, and metrics—yet in software, control rarely brings stability. It usually just slows feedback until systems fail silently. This article explores how governance differs from control: governance ensures the right things become visible at the right time through automated systems that tell the truth, not status reports. By replacing permission with visibility, technical leaders can manage feedback rather than people, creating sensor networks that surface misalignment early. Real stability looks noisy—with tests, builds, and human debate—but that noise is actually the sound of engineering excellence protecting the business from silent failure.</p>
</div>

Every leader wants two things at once:

🔹 Stability

🔹 Innovation

The problem? These two pull in opposite directions.

To get both, many organizations reach for *control* — the illusion of safety through process, meetings, and metrics.

But in software, control rarely brings stability.

It usually just slows the feedback loop until the system fails silently.

### Control Is Not Governance

Governance isn't about knowing everything.

It's about **ensuring that the right things become visible at the right time**.

Control means telling people what to do.

Governance means designing a system that *tells the truth* on its own.

In good engineering organizations, that truth comes from data, not status reports:

* Tests pass or fail.
* Pipelines run or stop.
* Monitoring shows reality in real time.

That's governance — not management.

### Replace Permission with Visibility

A healthy software system doesn't need pre-approval for every change.

It needs a pipeline that **catches bad changes automatically**.

| Old Control Mindset                | Modern Governance Practice                            |
| ---------------------------------- | ----------------------------------------------------- |
| "Let's review everything manually" | "Automated tests and gates protect production"        |
| "We must know every detail"        | "Dashboards show flow, errors, and uptime"            |
| "We approve releases"              | "We approve the *process* that ensures safe releases" |
| "We need meetings to align"        | "We need systems that surface misalignment early"     |

Governance isn't a bottleneck. It's a **sensor network**.

### The CTO's Real Job

The CTO who governs without control doesn't manage people directly.

They manage **feedback**.

Their job is to ensure that:

* Every change has a fast, automated signal.
* Quality metrics are visible to everyone.
* Technical debt is tracked like financial debt.
* Teams own their outcomes end-to-end.

If those systems exist, governance happens naturally — without command structures.

### The CEO's Dilemma

CEOs often mistake quiet for stability.

They see a lack of noise as a sign of control.

But in software, **silence means blindness**.

Real stability looks noisy — but not the way most executives think.

Yes, tests run. Builds fire. Logs roll. Alerts blink.

But those are just **signals**.

The real noise is **human**:

* Engineers questioning each other's assumptions while pairing or mobbing.
* Teams proposing spikes — "let's try this for two days and see what we learn."
* Designers challenging technical constraints.
* Developers debating trade-offs openly.
* Someone saying "I don't understand this" and three people stopping to explain.

(And no, not "code reviews" — those often devolve into toxic gatekeeping, another control fallacy disguised as quality.)

This is what a healthy engineering culture sounds like.

It's not chaotic — it's **collaborative turbulence**.

The technical artifacts don't create the noise.

**People talking, questioning, and experimenting** do.

When leadership mistakes that energy for disorder and tries to quiet it down, they kill the feedback loop.

The job isn't to silence the conversation — it's to make sure that energy converts into learning, decisions, and better software.

And yes, that means: writing code that gets thrown away. Tests that only serve understanding. Experiments that lead nowhere.

That's not waste — that's **thinking**.

The conversations are only the visible, audible part. The real thinking happens in the code itself.

Anyone demanding "fast features" while saying "talk to each other" hasn't understood that creating *and* discarding software is the thinking process, not a delay before the "real" programming.

### Trust, but Instrument

"Trust" sounds soft, but it's measurable.

A team that can deploy ten times a day with zero rollbacks is *governed*.

A team that needs five approvals and three committees for every release is *controlled* — and still unsafe.

The difference isn't trust alone — it's **instrumentation**.

Automate the feedback loops (tests, monitoring, deployment gates), not the people.

Free engineers from performing safety theater so they can focus on the work that actually matters: thinking, designing, experimenting, collaborating.

Governance scales through **architecture, automation, and accountability**, not hierarchy.

### The Paradox of Modern Leadership

The more you try to control engineers, the less you understand what's really happening.

The more you trust and instrument the system, the clearer everything becomes.

So stop asking for reports.

Ask for **evidence** — in the form of logs, metrics, and automated feedback.

And don't introduce a management framework that encroaches on developers' freedom to create and innovate.

Yes, many method coaches and framework authors will disagree. Their business model depends on believing software development is plannable like manufacturing.

But here's the critical point for leaders:

**Which approach delivers value faster?**

Frameworks can certainly reveal waste and produce signals. That's their value.

But they're not a lasting fix for bad software development practices.

Once the framework has done its job and exposed the problems, you need good development practices — not more ceremonies.

Frameworks that dictate *how* to work — mandatory standups, story point estimates, velocity tracking, sprint ceremonies — cost time and money.

They shift focus from **shipping software** to **performing process**.

More importantly: They increase your risk, not reduce it.

Why? Because they treat software development like manufacturing — with a clean separation between *preparing the work* (planning, estimation, design) and *doing the work* (coding, testing, deploying).

But software isn't an assembly line.

**Discovery and delivery are inseparable.**

You don't know what you're building until you start building it:

* Requirements clarify through code.
* Architecture emerges through experimentation.
* The "work" *is* the learning.

When you force developers to "finish thinking" before they start coding, you're not reducing risk — you're **delaying feedback** until it's expensive to act on.

And that costs you market opportunities while your competitors ship.

The teams that ship value fastest aren't the ones with the most ceremony.
They're the ones who can ship early and often — because their leadership invested in feedback systems, not process overhead.

And here's the economic reality: **With good practices and AI, you need smaller teams.**

Just as developers moved up from assembly to C, to Java/C# — each step letting them work at a higher level of abstraction — AI lifts them even higher today.

That means:

* Less coordination overhead across large teams.
* More direct collaboration between developers and subject matter experts.
* Faster decisions because fewer intermediaries are involved.

You don't need 50 developers coordinated through a framework.

You need 3-5 very good developers with AI tools, strong feedback, and direct access to business and domain experts.

That's not just faster — it's **cheaper by an order of magnitude**.

Frameworks promise to organize large teams.

Good practices with AI make large teams unnecessary.

This kind of thinking — strategic, architectural, product-aware thinking — becomes the most valuable part of software work.

The best teams don't split prepare-vs-do.

They evolve their own rhythms based on real feedback from their system and their users.

Give them clear outcomes, strong instrumentation, and the autonomy to figure out the path.

That's governance. Everything else is just overhead.

Governance is not knowing.

It's *seeing*.

#### TL;DR

* Control is human supervision.
* Governance is system feedback.

If you want stability *and* speed, don't tighten control — strengthen feedback.

That's how you govern without control.

<!-- Cross-language links intentionally omitted -->
