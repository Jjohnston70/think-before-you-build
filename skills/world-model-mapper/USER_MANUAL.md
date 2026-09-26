---
document_id: TNDS-PUB-011
title: "World Model Mapper User Manual"
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
consumed_by: [world-model-mapper]
corpus: none
related_assets: [TNDS-PUB-010]
tags: [world-model, user-manual, process-mapping]
notes: "How and when to run the framework, output formats, common patterns, troubleshooting."
---

# World Model Mapper - User Manual

## What This Is

A structured thinking tool that helps you analyze any business process, system, or tool through the lens of world model principles. It reveals where your systems are tracking shadows instead of reality, where decisions aren't mapped to actions, and where feedback loops are broken.

## Why It Matters

Most business automation does one of two things:
1. Moves information around (notifications, reports, dashboards)
2. Triggers actions based on simple rules (if X then Y)

Neither of these actually *models* how the business works. They don't predict consequences, learn from outcomes, or adapt when conditions change.

This skill helps you think like you're building a system that understands physics, not just shuffles data.

## When to Use This Skill

**When Scoping an Improvement**

Before you change a process, run it through this framework. The gap report tells you what to fix first and becomes the scope of the work.

Trigger phrases:
- "Let's map this process"
- "Analyze this system against world model principles"
- "Where are the gaps in this workflow?"
- "What state are we missing?"

**When Designing a New System or Tool**

Before building a tracker, dashboard, or automation, use this to make sure you capture the right state, map the right actions, and close the feedback loops.

Trigger phrases:
- "Help me design a system for [process]"
- "What should this tool track?"
- "How do I close the loop on this?"

**When Debugging Existing Systems**

If a system isn't delivering value or people aren't using it, the framework helps identify why. Often it's because:
- State is stale by the time decisions are made
- Actions aren't mapped to the state that triggers them
- No feedback tells you if the system is working

Trigger phrases:
- "Why isn't this working?"
- "What's missing from this system?"
- "Nobody is using this, diagnose it"

**For Teaching**

The framework is teachable. Walk a team through it on a whiteboard so they can think systematically about their own operations.

## How to Use This Skill

### Basic Usage

Start a conversation with Claude and describe the system you want to analyze:

```
I want to map our job scheduling process against world model principles. 
Walk me through the framework.
```

Claude will guide you through five phases:
1. Define the Target: What exactly are we analyzing?
2. State Discovery: What variables matter and are we tracking them?
3. Action Mapping: What decisions does this inform?
4. Transition Modeling: What are we predicting and how confident should we be?
5. Feedback Analysis: How do we know if we're right?

### Getting Good Results

**Be specific about the process.** "Our operations" is too broad. "How we schedule and dispatch technicians to jobs" is better.

**Bring real examples.** The framework works best when you can point to specific scenarios: "Last Tuesday we had three jobs run late because..."

**Challenge the "shadow vs. reality" distinction.** This is often where the biggest insights come from. A CRM "deal stage" is a shadow. The actual email timestamps showing engagement patterns are reality.

**Don't skip the feedback phase.** This is where most systems fail. If you can't answer "how would I know if this prediction was wrong?" then you have a broken feedback loop.

### Working Through Resistance

Sometimes you'll hit a phase and think "we don't have that" or "that doesn't apply." Push through it:

- "We don't track that" → That's a gap. Note it.
- "We can't predict that" → What would you need to track to predict it?
- "We don't have feedback on that" → How would you start capturing it?

The gaps are the point. The framework isn't supposed to validate your current system, it's supposed to reveal what's missing.

## Output Formats

The skill produces several outputs:

### State Inventory Table

| Variable | Tracked? | Refresh Rate | Leading/Lagging | Shadow/Reality | Priority Gap |
|----------|----------|--------------|-----------------|----------------|--------------|
| Job status | Yes | Manual update | Lagging | Shadow | - |
| Tech location | No | - | - | Reality | Critical |
| Drive time estimate | Yes | Static | Leading | Shadow | High |

### Action Map

| Decision | Decision Maker | Trigger Condition | Current Latency | Automation Candidate? |
|----------|----------------|-------------------|-----------------|----------------------|
| Reassign job | Dispatcher | Tech running late | 30+ min | Yes - with GPS |
| Notify customer | Customer service | Job delayed | 45+ min | Yes - auto-trigger |

### Transition Model

| Prediction | Confidence | Key Assumptions | Causal Chain Clarity | Brittleness Risk |
|------------|------------|-----------------|---------------------|------------------|
| Tech arrives at scheduled time | Low | No traffic, previous job on time | Unclear - no drive time model | High |

### Feedback Audit

| Prediction | Feedback Mechanism | Time to Feedback | Loop Status | Improvement Potential |
|------------|-------------------|------------------|-------------|----------------------|
| Arrival time | None systematic | Never (unless complaint) | Broken | High - log actual arrivals |

### Gap Report

Prioritized list of what's missing, ranked by impact × feasibility.

### Next Step

One specific, actionable thing to build or fix first.

## Using It Across an Improvement Project

### During First Conversations

Ask one question: "Can you describe what information would help you predict problems before they happen?" If they can't, the state gap is probably the real problem.

### During Assessment

Ask about current systems through this lens:
- What do they track? (State)
- What decisions do those inform? (Actions)
- How do they know if those decisions worked? (Feedback)

### During Mapping

Run the full framework on the core process. The outputs become the scope document.

### During Planning

Rank the gap report. "You have five critical gaps. This project closes three of them."

### During the Build

Each gap becomes a requirement. Each feedback loop becomes a measurable outcome.

## Advanced Usage

### Comparing Multiple Processes

Run the framework on two related processes and compare their maturity:
- Which has better state capture?
- Which has tighter feedback loops?
- Which is more brittle?

### Designing for Future State

Run the framework twice:
1. Current state (what exists)
2. Target state (what should exist)

The delta becomes your implementation roadmap.

### Teaching Clients

Walk clients through the framework on a whiteboard. It helps them understand why you're recommending certain changes and builds buy-in for data capture they might otherwise resist.

## Common Patterns

### The "Dashboard That Nobody Uses" Problem

Symptom: You built a dashboard but the client never looks at it.

Framework diagnosis: Usually one of:
- State is stale (refresh rate too slow to be useful)
- No action mapping (data exists but doesn't connect to decisions)
- Shadow data (they don't trust it because it's based on manual entries)

### The "Firefighting" Problem

Symptom: Client is always reacting to problems, never preventing them.

Framework diagnosis: Usually:
- All lagging indicators, no leading indicators
- Feedback loops are too slow (they find out about problems from customers)
- No transition model (they can't predict what happens next)

### The "Spreadsheet Addiction" Problem

Symptom: Client has elaborate spreadsheets they maintain manually.

Framework diagnosis: Usually:
- They've built their own primitive state model
- It works but doesn't scale (manual refresh)
- No automation because actions aren't mapped to triggers

The spreadsheet tells you what state they care about. Your job is to capture it automatically and connect it to actions.

## Troubleshooting

**"This feels too abstract"**

Ground it with a specific scenario. "Walk me through what happened last time a job ran late." Then map that scenario to the framework.

**"We don't have data for this"**

That's a finding, not a blocker. The framework reveals what data you *should* have. Capturing it becomes part of the implementation.

**"Our process is too messy to map"**

Start with one slice. "What happens between when a job is scheduled and when the tech arrives?" Messy processes often have a few critical transitions where state really matters.

**"The client doesn't think in these terms"**

Translate. Instead of "state space" say "the information you need to make decisions." Instead of "transition model" say "predicting what happens next." The concepts transfer even if the vocabulary doesn't.

## Key Takeaways

1. **Shadows vs. Reality**: Most systems track what people *say* happened, not what *actually* happened. Reality-grounded state is harder to capture but more valuable.

2. **Latency Kills**: State that's stale by the time you act on it is nearly worthless. Refresh rate matters as much as what you track.

3. **Feedback Closes the Loop**: A prediction without feedback is just a guess. Every prediction should have a mechanism to validate whether it was right.

4. **The Gap Is the Opportunity**: Don't be discouraged by missing state, broken loops, or weak predictions. That's exactly what you're building to fix.

5. **Start Concrete**: Pick one process, one decision, one prediction. Map it fully. Then expand.

True North Data Strategies LLC | truenorthstrategyops.com
