---
document_id: TNDS-PUB-023
title: "The Bearing Check: Framework Reference"
type: reference
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
tags: [framework, red-flags, navigation]
notes: "Philosophy, the two navigation approaches, and red flags per checkpoint."
---

# The Bearing Check - Framework Reference

## Origin

The Bearing Check synthesizes concepts from statistical decision theory, behavioral economics, and risk management into a practical validation framework. Adapted for operators and builders who need to make decisions under uncertainty without getting lost in theory.

A bearing check is what navigators do before committing to a course. You verify your position against multiple fixed reference points. If the references don't agree, you don't move until you understand why.

## The Seven Problems This Framework Solves

### Problem 1: Survivorship Bias (Winner-Only Dataset)
You only examine people who succeeded. You ignore the graveyard of people who did the same thing and failed. You mistake common behaviors for winning strategies.

### Problem 2: Human Reward-Seeking (Gambling Bias)
Humans secretly prefer exciting narratives. The brain maximizes emotional payoff, not truth. A lottery ticket is a mood purchase, not a rational investment.

### Problem 3: Wrong Variable Selection
People love finding a single factor. Real outcomes are messy. Watch for:
- Spurious correlations (things that move together but aren't causal)
- Confounders (hidden variables creating illusion of causation)
- Collinearity (multiple "causes" are same signal in disguise)
- Overfitting (pattern that was just historical noise)

### Problem 4: Ignoring Uncertainty
Point predictions are traps. Outcomes are probabilistic. The right question is not "Will this work?" but "What are the odds, and what happens if I'm wrong?"

### Problem 5: External Validity Failure
Even if a strategy works on average, it may require conditions you don't have: time horizon, emotional temperament, capital size, access to information, lifestyle constraints, risk tolerance, opportunity cost.

### Problem 6: Non-Stationarity
The world changes. Markets change. Industries change. When a strategy becomes popular, it gets competed away. You need a method that updates.

### Problem 7: All-In Fragility
Even a great model doesn't justify all-in. The correct response to uncertainty is sequential decision-making: start small, test, gather feedback, increase exposure when evidence accumulates, keep margin of safety.

## Two Navigation Approaches

### The Lost Navigator (fragile)
See destination → find someone who got there → copy their visible route → commit everything → hope conditions hold

### The Bearing Check (robust)
Verify current position → survey the terrain including hazards → test route assumptions → confirm you have supplies for the journey → advance in stages with decision points → maintain ability to adjust course

## Checkpoint Red Flags

### Checkpoint 1: Ground Truth
- "My situation is different" (usually isn't)
- Refuses to estimate base rate
- Only knows success stories
- Cites outlier examples as typical

### Checkpoint 2: Graveyard Recon
- Cannot name any failures
- Dismisses failures as "they did it wrong"
- Believes failures are irrelevant to their plan
- Only researched winners

### Checkpoint 3: Mechanism Check
- Explanation is tautological ("they succeeded because they had what it takes")
- Cannot separate behavior from mechanism
- Attributes success to single easily-copied factor
- Confuses correlation with causation

### Checkpoint 4: Fixed Points
- Plan depends entirely on timing or trends
- No durable competitive advantage identified
- Core factors are outside user's control
- Relies on conditions that could change

### Checkpoint 5: Odds Assessment
- Speaks in certainties
- Cannot articulate failure conditions
- Believes probability doesn't apply to their situation
- Rejects the premise that this could fail

### Checkpoint 6: Constraint Fit
- Ignores personal constraints when planning
- Assumes they can change constraints to fit strategy
- Borrowed strategy from someone with different resources
- Hasn't accounted for emotional cost

### Checkpoint 7: Staged Advance
- Wants to go all-in immediately
- No reversibility in plan
- Cannot articulate what evidence would change their mind
- Treats staged approach as lack of commitment

### Checkpoint 8: Pre-Mortem
- Hasn't imagined failure
- Failure would be catastrophic
- Plan only works once (not repeatable)
- No contingency for partial failure

True North Data Strategies LLC | truenorthstrategyops.com
