---
name: world-model-mapper
description: "Guided framework for mapping a business process, system, or tool against world model principles. Use when analyzing how an operation actually runs, designing a new system or tool, or diagnosing one nobody uses, to reveal gaps in state capture, action mapping, transition modeling, and feedback loops. Triggers on phrases like 'map this process,' 'analyze this system,' 'find the gaps,' 'world model analysis,' 'state space mapping,' 'why isn't this system working,' or 'what should this tool track.'"
metadata:
  document_id: TNDS-PUB-010
  title: "World Model Mapper"
  type: ai-asset
  domain: delivery
  tnds_layer: delivery
  version: "1.0"
  owner: Jacob Johnston
  organization: True North Data Strategies LLC
  created: 2026-09-25
  source: "Sanitized public edition of an internal TNDS skill, 2026-09-25"
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
  related_assets: [TNDS-PUB-011, TNDS-PUB-012, TNDS-PUB-013, TNDS-PUB-014, TNDS-PUB-015, TNDS-PUB-020]
  tags: [world-model, process-mapping, state-space, feedback-loops, shadow-vs-reality, gap-analysis]
  notes: "Five-phase interrogation: target, state, actions, transitions, feedback. Output is a prioritized gap report and one next step."
---

# World Model Mapper

A structured interrogation framework that stress-tests any business process or system against world model principles, revealing where state capture is weak, where actions aren't mapped to decisions, where predictions lack grounding, and where feedback loops are broken.

## Core Concept

Based on Yann LeCun's case for world models:
- **LLMs learn static knowledge** (what people have said)
- **World models learn dynamic rehearsal** (what happens next when you do something)

Most business systems track shadows (reports, deal stages, status fields) rather than reality (measurements, events, outcomes). This skill helps identify and close that gap.

## The Framework Components

Every operational system can be analyzed through four lenses:

1. **State Space (s_t)**: What matters right now, represented actionably
2. **Action Space (a_t)**: What decisions can actually be made
3. **Transition Function (s_t, a_t → s_{t+1})**: How actions change outcomes
4. **Feedback Loop**: Did the prediction match reality?

## Workflow

Guide the user through five phases. Complete each phase before moving to the next. Ask clarifying questions when needed.

### Phase 1: Define the Target

Establish what's being mapped:
- What system, module, or process are we analyzing?
- What's the primary outcome this system should influence?
- Who are the decision-makers this system serves?

Output: Clear scope statement and success criteria.

### Phase 2: State Discovery

Interrogate the current state representation:

**Currently Tracked:**
- What variables does the system currently capture?
- What's the refresh rate? (real-time, hourly, daily, weekly, manual)
- Are these leading indicators (predictive) or lagging indicators (historical)?

**Shadow vs. Reality Test:**
- Is each variable a shadow (what someone said/reported) or reality (direct measurement)?
- Example shadows: deal stage, customer satisfaction score, project status
- Example reality: email response time, payment timestamps, GPS location, sensor data

**Missing State:**
- What variables affect outcomes but aren't tracked?
- What would you need to know to predict the next problem before it happens?
- What information exists but isn't captured systematically?

**State Quality Audit:**
- Where is state information stale by the time it's used?
- Where do you have point-in-time snapshots but need trends?
- Where are you missing context that changes interpretation?

Output: State inventory table with columns: Variable | Tracked? | Refresh Rate | Leading/Lagging | Shadow/Reality | Priority Gap

### Phase 3: Action Mapping

Map the decision space:

**Decision Inventory:**
- What decisions does this system inform?
- Who makes each decision?
- What's the latency between state change and possible action?

**Action Classification:**
- Which actions should be automatic (no human needed)?
- Which actions should be surfaced for human decision?
- Which actions are currently impossible due to missing state?

**Intervention Points:**
- Where in the causal chain can you actually intervene?
- Which state changes are observable but not actionable?
- Where is prediction useful vs. merely interesting?

Output: Action map with columns: Decision | Decision Maker | Trigger Condition | Current Latency | Automation Candidate?

### Phase 4: Transition Modeling

Examine prediction quality:

**Explicit Predictions:**
- What outcomes is the system predicting (explicitly or implicitly)?
- What confidence level applies to each prediction?
- What assumptions underlie each prediction?

**Causal Chain Mapping:**
- For each predicted outcome, can you trace the causal mechanism?
- If you predict X, what's the actual chain of events that leads to X?
- Where are you pattern-matching on correlation vs. understanding causation?

**Brittleness Audit:**
- Where would a small deviation break the prediction?
- What edge cases aren't handled?
- Where does the system assume stability that doesn't exist?

**Narrative vs. Optimization Check:**
- Is the system producing a plan (narrative sequence) or optimizing under uncertainty?
- Does it weigh tradeoffs dynamically or follow fixed rules?
- Can it adjust when conditions change mid-execution?

Output: Transition model with columns: Prediction | Confidence | Key Assumptions | Causal Chain Clarity | Brittleness Risk

### Phase 5: Feedback Analysis

Audit the learning loop:

**Feedback Inventory:**
- For each prediction, how do you know if it was right?
- How long until you find out?
- Is that feedback captured systematically?

**Loop Status Classification:**
- Closed loop: Prediction → Outcome → Captured → Model Updated
- Open loop: Prediction → Outcome → Not Captured
- Delayed loop: Feedback exists but too late to be useful
- Broken loop: No mechanism to validate predictions

**The "Physics" of the Domain:**
- What are the hard constraints that don't change?
- Are these constraints explicit in the system or just assumed?
- Where might constraints be violated that the system wouldn't detect?

Output: Feedback audit with columns: Prediction | Feedback Mechanism | Time to Feedback | Loop Status | Improvement Potential

## Final Deliverables

After completing all phases, synthesize findings into:

### 1. Gap Report (Prioritized)

Rank gaps by impact × feasibility:
- Critical: Blocking core outcomes, fixable
- High: Significant impact, moderate effort
- Medium: Incremental improvement
- Low: Nice to have

### 2. State Architecture Diagram

A Mermaid diagram or a short written description showing:
- Current state variables and their sources
- Missing state variables (marked)
- Data flow between components
- Feedback loops (closed, open, broken)

### 3. Recommended Next Step

One concrete action to take first. Be specific:
- What to build or fix
- What data to start capturing
- What feedback loop to close
- Expected impact

## Quality Checks

Before finalizing, verify:
- [ ] Every tracked variable classified as shadow or reality
- [ ] Every decision mapped to a trigger condition
- [ ] Every prediction has an identified feedback mechanism (or marked as missing)
- [ ] At least one "physics constraint" identified for the domain
- [ ] Gap report prioritized by impact × feasibility
- [ ] Next step is specific and actionable

## Example Application

**Target:** Fleet management for field service company

**State Discovery Findings:**
- Tracking: Job status, technician assignment, scheduled time
- Missing: Real-time location, actual drive times, job duration variance
- Shadow vs. Reality: Job status is shadow (tech updates manually), GPS would be reality

**Action Mapping Findings:**
- Decision: Reassign jobs when running late
- Current latency: Tech calls dispatch → dispatch calls customer → 30+ min
- With real-time location: Auto-detect delay → auto-notify customer → 2 min

**Transition Model Findings:**
- Implicit prediction: "Scheduled time = arrival time"
- Reality: Traffic, previous job overrun, lunch breaks
- Brittleness: Any deviation from schedule cascades unpredictably

**Feedback Findings:**
- No systematic capture of predicted vs. actual arrival
- Customer complaints are only feedback (too late, too sparse)
- Loop status: Broken

**Gap Report:**
1. Critical: Add real-time location tracking
2. High: Capture actual arrival times vs. scheduled
3. Medium: Build drive time prediction model
4. Low: Customer notification automation

**Next Step:** Implement GPS tracking on tech vehicles, log arrival timestamps automatically.

True North Data Strategies LLC | truenorthstrategyops.com
