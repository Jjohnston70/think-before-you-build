---
document_id: TNDS-PUB-013
title: "Feedback Loop Patterns"
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
consumed_by: [world-model-mapper]
corpus: none
related_assets: [TNDS-PUB-010]
tags: [feedback-loops, closed-loop, proxy-metrics]
notes: "Classify loops as closed, open, delayed, or proxy, and how to fix each."
---

# Feedback Loop Patterns

How to identify, classify, and fix feedback loops in business systems.

## Loop Status Classification

### Closed Loop (Healthy)

```
Prediction → Action → Outcome → Captured → Model Updated
```

Example: Weather app predicts rain → You bring umbrella → It rains → App logs accuracy → Forecast model improves

Business example: System predicts job will take 2 hours → Tech does job → Actual time logged automatically → Future estimates adjust based on history

**Characteristics:**
- Outcome is captured automatically
- Feedback reaches the prediction system
- Future predictions incorporate learning
- Continuous improvement visible

### Open Loop (Broken)

```
Prediction → Action → Outcome → [Lost]
```

Example: You estimate project takes 2 weeks → Work happens → Project ends → No one records actual duration → Next estimate is still a guess

**Characteristics:**
- Predictions made but never validated
- "We think it's working but we don't actually know"
- Same mistakes repeated
- Estimation never improves

### Delayed Loop (Problematic)

```
Prediction → Action → Outcome → [Long Delay] → Captured → [Too Late] → Model
```

Example: Marketing predicts campaign will drive sales → Campaign runs → Sales happen (maybe) → Attribution figured out 6 months later → Campaign already over

**Characteristics:**
- Feedback exists but arrives too late to act on
- Learning happens but can't course-correct
- Post-mortems instead of real-time adjustment

### Proxy Loop (Risky)

```
Prediction → Action → Outcome A (real) → Outcome B (proxy) captured → Model
```

Example: Sales training predicts better close rates → Training delivered → Actual close rates unknown for months → Survey says reps "feel more confident" → Training deemed successful

**Characteristics:**
- Measuring something related but not the actual outcome
- Proxy may not correlate with reality
- False confidence in effectiveness

## Common Business Loops and Their Status

| System | Prediction | Typical Loop Status | Why |
|--------|------------|---------------------|-----|
| Sales forecasting | Deal will close this quarter | Open | Win/loss rarely traced back to forecast accuracy |
| Project estimation | Will take X hours | Open or Delayed | Actual hours often not tracked |
| Hiring | Candidate will perform well | Delayed | Performance review 6-12 months later |
| Marketing | Campaign will drive conversions | Proxy | Clicks measured, revenue attribution unclear |
| Scheduling | Job will finish on time | Open | Actual completion time not captured |
| Inventory | Will need X units next month | Closed (usually) | Stockouts and overstock visible immediately |
| Customer churn | Customer will leave | Delayed | Takes months to validate; unclear what caused it |

## Closing Open Loops

### Step 1: Identify the Real Outcome

Ask: "What actually happens that we care about?"

Not "customer satisfied" → Customer renewed contract
Not "lead qualified" → Lead became paying customer
Not "project complete" → Deliverables accepted and paid

### Step 2: Find the Timestamp

When does the outcome become knowable? Build capture at that moment.

- Job completion: When tech marks done + photo uploaded
- Payment received: When bank confirms deposit
- Contract signed: When DocuSign webhook fires
- Customer churned: When subscription cancelled or renewal declined

### Step 3: Connect Back to Prediction

Create the link:
- Log the original prediction with a unique ID
- When outcome occurs, associate it with that prediction
- Calculate accuracy (predicted vs. actual)
- Surface accuracy metrics somewhere visible

### Step 4: Feed Forward

Use accuracy data:
- Adjust confidence in future predictions
- Identify systematic biases (always optimistic? always pessimistic?)
- Train humans making predictions to calibrate better

## Shortening Delayed Loops

### Add Leading Indicators

If final outcome takes 6 months, what happens at 1 month that predicts it?

- New hire performance: 90-day metrics instead of annual review
- Sales campaign: Pipeline movement in first 2 weeks instead of Q-end revenue
- Customer health: Usage patterns this week instead of renewal 11 months away

### Create Intermediate Checkpoints

Break long predictions into shorter ones:
- Instead of: "Project will deliver in 6 months"
- Track: "Sprint 1 will complete these features by Friday"

Each checkpoint is a mini feedback loop that keeps the overall system calibrated.

### Implement Early Warning Signals

If you can't speed up the outcome, detect deviation early:
- Project tracking: Velocity declining = delivery at risk
- Customer health: Support tickets spiking = churn risk rising
- Sales: Response time increasing = deal cooling

## Fixing Proxy Loops

### Validate the Proxy

Before trusting a proxy, prove it correlates:
- Run historical analysis: Did high proxy scores actually predict good outcomes?
- A/B test: Does improving the proxy improve real outcomes?
- Watch for Goodhart's Law: When proxy becomes target, it stops being useful

### Move Toward Reality

| Proxy | Reality Alternative |
|-------|---------------------|
| Customer satisfaction survey | Renewal rate, expansion revenue |
| Employee engagement score | Retention rate, productivity metrics |
| Lead quality score | Conversion rate, deal size |
| Training completion | On-the-job performance change |
| Website traffic | Revenue per visitor |

### Accept Proxy Limitations

Sometimes proxies are all you have. Be honest:
- "We measure X as a proxy for Y"
- "We believe but have not proven they correlate"
- "We'll validate this assumption by [date]"

## Red Flags: Signs of Broken Feedback

- "We've always done it this way" (no evidence it works)
- "Customers seem happy" (no measurement)
- "Our estimates are usually pretty good" (no tracking)
- "That's just how long it takes" (no optimization)
- "We'll know at the end of the quarter" (delayed loop)
- "The survey says it's working" (proxy loop)

## The Feedback Audit Question Set

For any prediction your system makes:

1. What outcome would prove the prediction right or wrong?
2. When does that outcome become knowable?
3. Is that outcome captured in a system?
4. Does the captured outcome connect back to the original prediction?
5. Does prediction accuracy get reviewed? By whom? How often?
6. Do future predictions change based on past accuracy?

If you can't answer all six, your loop is broken.

True North Data Strategies LLC | truenorthstrategyops.com
