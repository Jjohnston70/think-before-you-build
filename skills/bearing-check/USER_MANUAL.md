---
document_id: TNDS-PUB-024
title: "The Bearing Check User Manual"
type: user-manual
domain: delivery
tnds_layer: delivery
version: "1.0"
owner: Jacob Johnston
organization: True North Data Strategies LLC
created: 2026-09-25
source: "Sanitized public edition of an internal TNDS asset, 2026-09-25"
status: draft
last_updated: 2026-09-25
review_due: 2027-03-25
supersedes: null
superseded_by: null
classification: public
authority: reference
approver: null
use_with: [claude, claude-code, cowork]
consumed_by: [bearing-check]
corpus: none
related_assets: [TNDS-PUB-020]
tags: [bearing-check, user-manual, decision-making]
notes: "How to invoke the framework, full vs. quick pass, the numbers rule, and attribution."
---

# The Bearing Check, User Manual

## What This Is

The Bearing Check is a decision validation framework. It helps you pressure-test a decision before committing resources. Think of it as a pre-flight checklist for major life and business decisions.

The framework synthesizes concepts from statistical decision theory, behavioral economics, and risk management into eight sequential checkpoints. A bearing check is what a navigator does before committing to a course: verify your position against several fixed reference points, and if they disagree, do not move until you understand why.

## How to Use It

Install the plugin, then ask Claude about a decision. The skill triggers on phrases like:

- "Should I..."
- "Is this a good idea..."
- "Help me decide..."
- "Evaluate this strategy..."
- "What are the risks of..."
- "Run a bearing check on..."

You can also use `references/checkpoints.md` on its own as a personal checklist.

## The Eight Checkpoints

| # | Checkpoint | Core Question |
|---|------------|---------------|
| 1 | Ground Truth | What's the actual success rate for people like me? |
| 2 | Graveyard Recon | Who tried this and failed? What happened? |
| 3 | Mechanism Check | What actually caused success? Would it work without hidden factors? |
| 4 | Fixed Points | Which success factors are stable vs. trendy? |
| 5 | Odds Assessment | What are the real odds? What happens if I'm wrong? |
| 6 | Constraint Fit | Do my resources and temperament match this strategy? |
| 7 | Staged Advance | What's the smallest test I can run first? |
| 8 | Pre-Mortem | If I fail, what caused it? Can I survive it? |

## Full Pass vs. Quick Pass

**Full framework (all eight):** major decisions with significant downside. Career pivots, large investments, business bets, partnership commitments, hiring key roles, major contracts.

**Quick pass (checkpoints 1, 5, 7):** smaller decisions where the base rate, the odds, and a staged test give enough rigor.

**Single checkpoint:** when the question is about one aspect. "What's the success rate?" is Checkpoint 1. "What could go wrong?" is Checkpoint 8.

## A Rule About Numbers

Checkpoints 1 and 5 run on numbers. Claude looks them up in the session and shows the source and its date. A base rate stated from memory is a guess dressed up as a fact, which is the exact error this framework exists to catch.

## Reference Files

| File | What it holds | Use when |
|---|---|---|
| `references/checkpoints.md` | Each checkpoint with key questions, a worked example, and common mistakes | Teaching the framework or wanting detailed examples |
| `references/cognitive-biases.md` | The seven traps the framework counters | Explaining why a checkpoint matters |
| `references/framework.md` | Philosophy, the two navigation approaches, red flags per checkpoint | Quick red-flag detection |

## Tailoring by Audience

| Audience | Lean on checkpoints |
|---|---|
| Investors and finance | 1, 5, 7, 8: base rates, odds, staged bets, survivability |
| Career changers | 1, 3, 6: base rates, mechanism vs. behavior, constraint fit |
| Founders and builders | 2, 4, 7: failure analysis, stable factors, staged testing |

To add examples for your own field, edit `references/checkpoints.md`.

## Attribution

The Bearing Check synthesizes established concepts from statistical decision theory, behavioral economics, and risk management: base rates, survivorship bias, pre-mortems, and staged bets. The original eight-step structure was inspired by an article published in the Data Science Collective on Medium, then renamed, rebuilt around navigation language, and extended.

True North Data Strategies LLC | truenorthstrategyops.com
