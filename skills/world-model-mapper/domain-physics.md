---
document_id: TNDS-PUB-012
title: "Domain Physics Reference"
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
tags: [domain-physics, constraints, anomaly-detection]
notes: "Hard constraints by domain and how to encode them."
---

# Domain Physics Reference

Every business domain has "physics", hard constraints that don't change regardless of what anyone wants or reports. Identifying these grounds your world model in reality.

## Why Physics Matters

The point: a constraint does not change because someone reported it differently.

In business terms: Your system should know what's actually possible, not just what people say they'll do.

## Common Domain Physics

### Field Service / Trades

| Constraint | Implication |
|------------|-------------|
| Drive time between locations is fixed by geography and traffic | Can't schedule jobs faster than travel allows |
| Technician hours are finite (8-10 productive hours/day) | Overbooking creates cascade failures |
| Parts either exist in inventory or they don't | "We'll figure it out" isn't a parts strategy |
| Weather affects outdoor work | Schedule buffers needed for weather-dependent jobs |
| Permits have fixed processing times | Can't start work before permit clears |
| Daylight hours constrain exterior work | Winter schedules must differ from summer |

### Financial Operations

| Constraint | Implication |
|------------|-------------|
| Standard ACH transfers take one or more business days to settle | "Money sent" ≠ "money available" |
| Payroll must be funded before it runs | Cash flow timing is non-negotiable |
| Tax deadlines are fixed | Late filing has hard penalties |
| Credit card processing has fees | Margin calculations must include payment costs |
| Float exists between invoice and collection | AR timing affects cash position |

### Sales / Revenue

| Constraint | Implication |
|------------|-------------|
| Decision-makers have limited attention | More outreach ≠ more deals |
| Budget cycles are annual for most orgs | Timing matters more than pitch quality |
| Contracts require signature authority | "Interested" ≠ "can buy" |
| Competitors exist | Your proposal isn't evaluated in isolation |
| Reference checks take time | Can't rush enterprise deals past a point |

### Operations / Manufacturing

| Constraint | Implication |
|------------|-------------|
| Machines have throughput limits | Can't exceed capacity without adding equipment |
| Changeover time between products is fixed | Small batches have overhead cost |
| Quality defects have rework time | Rushing increases total time |
| Supply chain lead times are real | Can't manufacture without materials |
| Skilled labor takes time to train | Scaling requires advance planning |

### Real Estate

| Constraint | Implication |
|------------|-------------|
| Inspection periods are contractual | Can't skip due diligence |
| Financing approval takes time | Cash buyers move faster for a reason |
| Title search is required | Can't close without clear title |
| Appraisal must support price | Financing constrained by appraised value |
| Occupancy rules vary by jurisdiction | Can't assume same rules everywhere |

## How to Identify Physics in Any Domain

Ask these questions:

1. **What can't be changed by anyone's decision?**
   - Time constraints (processing, shipping, curing, growing)
   - Physical limits (distance, capacity, strength)
   - Regulatory requirements (permits, licenses, filings)

2. **What happens if you try to violate the constraint?**
   - If violation is impossible → Hard physics
   - If violation has severe consequences → Soft physics (treat as hard)
   - If violation is inconvenient but manageable → Not physics, just preference

3. **What would an experienced operator never try to do?**
   - Veterans know the physics intuitively
   - Ask: "What would a 20-year veteran warn a rookie about?"

4. **What do customers complain about that can't actually be fixed?**
   - "Why does this take so long?" often reveals physics
   - The answer "because that's how long it takes" indicates a constraint

## Using Physics in Your World Model

### Make Constraints Explicit

Don't assume the system "knows" physics. Encode it:
- Maximum jobs per tech per day
- Minimum time between appointments
- Payment processing delays
- Required approval chains

### Validate Against Physics

When predictions violate physics, flag them:
- "Schedule shows 12 jobs for a tech that can do 8"
- "Cash flow shows payment clearing same day as invoice"
- "Timeline shows permit approval in 2 days (typical: 2 weeks)"

### Use Physics for Anomaly Detection

Physics violations in actual data indicate data quality issues:
- Job completion time of 3 minutes for a 2-hour job → Timestamp error
- Two jobs completed simultaneously by one tech → Data entry mistake
- Payment received before invoice sent → System sync issue

## The "What If Physics Changed?" Test

For any constraint you've identified, ask: "What if this weren't true?"

If the answer is "our whole business model changes," it's real physics.

If the answer is "we'd save some money," it's preference, not physics.

True North Data Strategies LLC | truenorthstrategyops.com
