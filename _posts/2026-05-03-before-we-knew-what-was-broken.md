---
layout: post
title: 'Before We Knew What Was Broken'
date: 2026-05-03 09:00:00 +0530
description: 'Why the first visible failure is not always the whole problem, and how shallow diagnosis can create more rules, workarounds, and misplaced blame.'
excerpt: 'The person at the point of failure may simply be where a much larger problem became impossible to hide.'
categories:
  - writing
tags:
  - systems
  - problem-solving
  - software
  - organizations
  - people
---

We are often rewarded for solving problems quickly. We are rarely rewarded for asking whether the problem has been understood correctly.

This has conditioned us to treat problem-solving as a reflex rather than a process. When a customer complains, we may add a new feature. When data looks wrong, we may introduce another validation rule. When employees leave, retention benefits may be announced.

Everyone does this. We want relief. We want movement. We want to feel useful. So we reach for the nearest explanation.

And these responses feel productive — they are visible and measurable. They are fast, and they offer the immediate satisfaction of a completed task. But often, we are simply solving the version of the problem that is easiest to see.

Consider a delayed release. The delay is what everyone experiences. It disrupts plans, frustrates customers, and places the team under pressure. It is where the pain becomes visible.

An initial investigation may point to repeated defects. They appear to explain the delay, so the natural response is to improve testing, add reviews, or ask the team to be more careful.

But the defects may have begun earlier. Perhaps the requirements kept changing. Perhaps important decisions were left unresolved. Perhaps people did not feel safe asking questions that might make them look inexperienced or slow.

At that point, the problem is no longer only a collection of defects. It includes the conditions that allow the same pattern to return.

There may not even be one hidden cause beneath it all. Several decisions, constraints, and adaptations that made sense individually may have combined to produce the failure.

When we do not look deeply enough, these patterns tend to repeat. A superficial diagnosis can lead to more rules, more workarounds, and more quick fixes.

When we misunderstand the problem, the solution often becomes another layer that people must learn to work around. And the person nearest the failure is often treated as its cause. A developer may be labelled careless because one module repeatedly produces defects. Or a customer struggling to understand the product may simply be called difficult.

Individual responsibility matters, but it should not become an excuse for avoiding the system around the individual. Visibility is not the same as responsibility. The person at the point of failure may simply be where a much larger problem became impossible to hide.

Acting quickly is not always wrong. Sometimes the immediate damage must be contained before anything deeper can be understood. The danger begins when containment is mistaken for understanding, and the temporary response becomes the final explanation.

The goal is not to delay action indefinitely or to search endlessly for a perfect root cause. It is to resist the temptation to confuse the first visible failure with the whole problem.

And maybe to admit, if only to ourselves, that we still do not understand what has truly broken.
