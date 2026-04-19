---
date: 2026-06-08
title: AI Is Writing More Code Than Your QA Team Can Test
seo-description: AI is making developers faster. The math for QA engineers has quietly broken. Here's why "hire another QA" is the wrong answer, and what quality engineering actually looks like when you can't outrun the velocity.
tags:
  - qa
  - ai
  - engineering
status: draft
---

There is a specific kind of meeting that happens at some point in every team that adopts AI-assisted development.

Someone looks at the sprint velocity and says: we're shipping more than ever. Then someone else, usually the QA engineer, says: yes, and I haven't slept properly in two weeks.

The room goes quiet in that way rooms go quiet when everyone agrees something is wrong but no one wants to say it out loud.

The math has broken.

***

The numbers are not subtle. Stack Overflow's 2025 Developer Survey reports that 84% of developers either use or plan to use AI tools, and 51% of professionals use them every day. GitHub's Octoverse describes a sharp rise in pull requests, commits, and AI-assisted projects. Developers are producing more.

But code volume and code quality are not the same metric, and they stopped moving together.

DORA 2024 is honest about the tradeoff: AI raises individual productivity and developer satisfaction, but can carry unexpected costs for stability and throughput. A study accepted at ISSRE 2025 analyzed more than 500,000 Python and Java samples and found that AI-generated code has a distinct defect profile, one with a disproportionate share of high-risk security vulnerabilities.

So the situation is roughly: more code, more changes, more PRs, a different risk shape, and the same QA engineer sitting at the end of the funnel holding a clipboard.

The way that scales is: hire another QA engineer.

That is not a strategy. That is a staffing patch on an engineering problem.

***

Here is the thing I keep coming back to.

The framing that breaks is **QA as the last human filter before release.** If quality is something one person checks before shipping, then more velocity equals more QA pressure, and the only response is more humans.

But there is a different framing: **QA as the engineering of quality, built into the system of development itself.**

The difference is enormous.

In the second framing, a QA engineer doesn't find a bug and move on. They find a bug and ask: *what mechanism should have caught this earlier?* Then they build that mechanism. An automated test, a contract check, a lint rule, a CI gate, a production monitor, a change to the definition of done, a review checklist, a test data generator.

The bug turns into a class of prevented bugs.

If a bug is found once and can still occur through the same gap, the QA experience was not scaled. If the bug becomes a rule, a test, a signal, or a product metric, it begins to compound.

That is the direction. QA as accumulated engineering capital, not manual heroism.

***

This is also where AI fits into the picture, though probably not in the way most job-anxiety conversations frame it.

The naive version says: AI will write all the tests, AI will check everything, QA is finished.

The more realistic version is that AI becomes a cheap generator of hypotheses, edge cases, test scenarios, data, and diff analyses. Fast, cheap, available at 3am when no human wants to think about boundary conditions in a payment form.

But here is the trap. AI can generate a lot of moot tests just as quickly as it generates useful ones. Tests that pass but prove nothing. Tests that are fragile against implementation detail. Tests that cover the happy path seventeen ways while the edge case that will hit production next Tuesday remains invisible.

The person who tells the difference is not replaceable.

A strong QA engineer of the near future is not someone who asks AI to write tests. It's someone who looks at the output and says: *this test has no diagnostic value. This oracle is weak. This is testing an implementation detail, not a behavior. This needs a contract test, not a UI test. This needs a synthetic monitor in production, not a staged regression.*

That judgment is the leverage point. And it does not come from prompting.

***

The skills that actually compound right now are worth naming specifically.

**Engineering foundation:** TypeScript or Python, Playwright or Cypress, API testing, CI/CD pipelines, Docker, SQL. Not because you need to automate everything, but because you need to speak the language of the system you're protecting.

**Test strategy:** risk-based testing, boundary analysis, state modeling, pairwise, mutation testing, test impact analysis. The ability to look at a set of changes and say: here is where the risk actually lives, here is what we need to check, and here is what we can skip.

**Observability:** logs, metrics, traces, dashboards, SLO/SLA, product analytics, incident review. A QA engineer who can read production is stronger than one who can only see staging. Not because production is where you want to find bugs, but because production is where reality lives.

**AI-assisted workflows:** not "ask ChatGPT to write a test," but a repeatable process. Prompt templates with structured context from requirements and diffs. Scenario generation with documented assumptions. Traceability from scenario back to intent. Hallucination checks on the generated output. The difference between using AI as a shortcut and using it as a force multiplier is the presence or absence of a process.

**Domain expertise.** The deeper you understand the product, the users, the money, and the business invariants, the harder you are to replace. An AI agent doesn't know why a particular rounding behavior in a billing flow is a legal problem. You do.

***

There is also a shift in where quality work happens that is worth paying attention to.

Classic QA lives before release. But modern products increasingly require quality *after* release: feature flags, canary deployments, synthetic monitoring, crash-free sessions, funnel metrics, anomaly detection, session replay, rollback automation.

When the volume of changes makes it impossible to predict everything upfront, quality becomes less about "we tested everything before shipping" and more about: we limited the blast radius, we detect degradations quickly, we can roll back, we know which user scenarios were affected, and we turn production signals into new checks.

The QA engineer who understands this becomes something different. Not just testing before the merge, but watching what happens after.

***

The most honest thing I can say about where this is heading: the profession is going to split.

On one side: QA as execution of predefined test cases, regression checklists, manual steps with expected results. This role is under real pressure. Not because it's unimportant, but because it's exactly what AI tools are being optimized to replace. Square Enix publicly set a target of automating 70% of QA and debugging tasks in game development by the end of 2027. Even if that number is optimistic, the direction is clear.

On the other side: **Quality Engineering** - the work of designing the system that makes bad quality expensive, visible, and hard to ship. Building the mechanisms. Managing the AI tools that run them. Reading production signals. Setting the oracle. Deciding what actually matters.

This is not a smaller role. It might be a more important one.

Because the more AI-generated code there is, the more valuable it is to have someone who understands exactly where the quality system is lying to you.

***

The simplest way I know to frame the real goal:

Every bug found by QA should produce two things. A ticket, yes. But also an answer to: *what systematic mechanism should have caught this earlier?*

Add an automated test. Change the definition of done. Add a lint rule. Update the monitoring. Add a test data case. Change the requirement template. Add a production alert. Update the risk checklist.

Over time, that question transforms what QA means. Not a manual force, scaling linearly with team size. But a compounding system, getting smarter with every release.

The goal isn't a QA engineer who checks more things faster. It's an engineering culture that needs less heroism from QA every cycle, because it has learned to prevent that class of problem itself.

That is what scaling quality actually looks like.

And it has nothing to do with headcount.
