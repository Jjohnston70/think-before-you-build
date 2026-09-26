---
document_id: TNDS-PUB-022
title: "Cognitive Biases and Decision Traps"
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
tags: [biases, survivorship, non-stationarity]
notes: "The seven traps the framework counters."
---

# Cognitive Biases and Decision Traps

This framework addresses seven core problems in how people learn from success and make decisions.

## Problem 1: Survivorship Bias (The Winner-Only Dataset)

### What It Is
When you only examine people who succeeded, you're sampling the world in a biased way. You're ignoring the graveyard of people who did the same thing and failed.

### How It Manifests
- "Successful people wake up at 5am" (ignoring unsuccessful people who also wake at 5am)
- "This investment strategy made millionaires" (ignoring everyone who lost money)
- "Dropouts become billionaires" (ignoring millions of struggling dropouts)

### The Trap
If you only study winners, you'll mistake common behaviors for winning strategies.

### Framework Response
Checkpoint 2 (Graveyard Recon) directly counters this by requiring active search for failures.

---

## Problem 2: Winner's Curse (Extreme Results Include Extreme Luck)

### What It Is
Even when a winner has skill, extreme performance usually contains a big luck component. If you copy the strategy expecting the same outcome, you're often chasing noise.

### How It Manifests
- "The best-performing fund last year" is frequently a warning sign, not a buy signal
- "Overnight success" stories sound replicable but aren't - you're looking at a lucky tail event

### The Trap
Many "winner behaviors" are just common behaviors. Plenty of people drink wine. A few live to 99. You're seeing the overlap and calling it causation.

### Framework Response
Checkpoints 1 and 3 address this by requiring ground truth and mechanism analysis.

---

## Problem 3: The Gambling Bias (We Prefer Exciting Narratives)

### What It Is
Even when failures are visible, people avoid them. Not because they can't understand, but because humans are reward-driven. The brain doesn't maximize truth - it often maximizes emotional payoff.

### How It Manifests
- You can show people negative samples and base rates; they still chase the one shiny story
- A lottery ticket is not a rational investment - it's a mood purchase
- "Hot stock tips" and "get rich fast" schemes persist despite clear evidence they fail

### The Trap
If your decision method is fueled by adrenaline, you're not modeling reality - you're buying a fantasy.

### Framework Response
Checkpoint 5 (Odds Assessment) forces rational evaluation over emotional response.

---

## Problem 4: Wrong Variable Selection (Correlation, Collinearity, and Fake Explanations)

### What It Is
People love to find a single factor: a habit, a tool, a skill. But real outcomes are messy. Many factors move together. Some are merely proxies. Some are irrelevant.

### Types of Errors
- **Spurious correlations:** Things that move together but aren't causal
- **Confounders:** Hidden variables that create the illusion of causation
- **Collinearity:** Multiple "causes" are really the same signal in disguise
- **Overfitting:** A "pattern" that was just historical noise

### Example
You notice high performers "wake up early." But if you copy the wake-up time without the underlying structure (energy management, protected focus time, schedule control), you copy the surface, not the engine.

### The Rule
A good explanation must survive contact with alternative explanations.

### Framework Response
Checkpoint 3 (Mechanism Check) and Checkpoint 4 (Fixed Points) address this.

---

## Problem 5: Ignoring Uncertainty

### What It Is
Even if you picked the right variables, outcomes are probabilistic. Point predictions are a trap - you need ranges.

### How It Manifests
- Decisions made as if the future is a single line: "If I do X, I will get Y"
- No consideration of downside scenarios
- Overconfidence in predictions

### The Right Question
Not "Will this work?" but "What are the odds, and what happens if I'm wrong?"

### Framework Response
Checkpoint 5 (Odds Assessment) replaces binary thinking with probability ranges.

---

## Problem 6: External Validity Problems (True Rules Might Not Apply to You)

### What It Is
Even if a strategy works on average, it may require conditions you don't have. What works in general may not work for you specifically.

### Constraint Mismatches
- **Time horizon:** Strategy needs 20 years; you need results in 5
- **Emotional temperament:** Strategy requires holding through 50% drawdowns; you panic at 10%
- **Capital size:** Strategy needs scale to work; you don't have it
- **Access to information:** Strategy requires insider knowledge you lack
- **Lifestyle constraints:** Strategy assumes flexibility you don't have
- **Risk tolerance:** Strategy assumes you can afford to lose; you can't
- **Opportunity cost:** Strategy ignores what you're giving up

### The Trap
Copying a strategy without copying its constraints is like copying a champion's training plan without having their body, coach, or recovery capacity.

### Framework Response
Checkpoint 6 (Constraint Fit) forces constraint matching.

---

## Problem 7: Non-Stationarity (The World Changes)

### What It Is
Even if something works for you today, the environment can shift. Markets change. Industries change. Hiring changes. Culture changes. Regulation changes.

### The Brutal Dynamic
When a strategy becomes popular, it gets competed away.

### Examples
- A course becomes famous -> it floods the market -> the signal weakens
- A content style becomes popular -> everyone copies it -> attention shifts
- An arbitrage opportunity exists -> too many people find it -> margins disappear

### The Trap
You need a method that doesn't depend on one eternal formula. You need a method that updates.

### Framework Response
Checkpoint 7 (Staged Advance) and Checkpoint 8 (Pre-Mortem) create feedback loops and adaptation mechanisms.

---

## Summary: The Seven Traps

| Trap | What Goes Wrong | Framework Counter |
|------|----------------|-------------------|
| Survivorship Bias | Only seeing winners | Checkpoint 2: Graveyard Recon |
| Winner's Curse | Confusing luck for skill | Checkpoints 1, 3: Ground Truth, Mechanism Check |
| Gambling Bias | Emotional over rational | Checkpoint 5: Odds Assessment |
| Wrong Variables | Correlation vs. causation | Checkpoints 3, 4: Mechanism Check, Fixed Points |
| Ignoring Uncertainty | Point predictions | Checkpoint 5: Odds Assessment |
| External Validity | Doesn't fit your constraints | Checkpoint 6: Constraint Fit |
| Non-Stationarity | World changes | Checkpoints 7, 8: Staged Advance, Pre-Mortem |

---

## The Meta-Lesson

Most people are not short on effort. They're short on method.

They spend years copying outcomes without understanding the decision structure that produced them. They confuse a visible habit with a hidden mechanism. They ignore probability. They ignore fit. They ignore drift. They go all-in because it feels heroic.

That's not courage. That's an unpriced risk.

True North Data Strategies LLC | truenorthstrategyops.com
