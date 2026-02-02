# Topic 1 — Project Management (Revision Notes)

## Why project management matters in software
- Software projects are constrained by **budget**, **schedule**, and **quality**.
- Common failure modes: late delivery, cost overruns, and failing to meet customer expectations.
- Software management is hard because:
  - Progress is **intangible** (hard to “see” completion).
  - Projects are often **one‑off** (unique requirements and context).
  - Processes are **variable** and organisation‑specific.

## The Triple Constraint (Time–Cost–Scope) and Quality
- **Time**: deadlines, schedule.
- **Cost**: budget, resources, staffing.
- **Scope**: features and tasks to be delivered.
- Key idea: these constraints are **interdependent**.
  - If **scope increases** and time/cost don’t change, quality suffers or delivery slips.
  - If **time is reduced**, you usually need to increase cost (more resources) or reduce scope.

## Universal management activities
- **Proposal writing**: needed when bidding for contracts.
- **Project planning**: defining tasks, dependencies, milestones.
- **Risk management**: identify, assess, mitigate, and monitor risks.
- **People management**: select team members, lead and coordinate work.
- **Reporting**: communicate progress; meetings and reviews.

## Scope management
Purpose: define and control what is included (and excluded) to prevent overruns.
Core activities:
- **Define scope** (boundaries and deliverables)
- **Verify scope** (confirm acceptance of deliverables)
- **Control scope** (manage scope changes)

## Estimation basics
### 1) Size estimation
Common measures and characteristics:
- **LOC / KLOC**: counts source lines.
  - Pros: simple, objective.
  - Cons: language‑dependent, encourages verbosity.
- **Function Points (FP)**: measures user‑visible functions (inputs, outputs, interfaces), adjusted by complexity.
  - Pros: language‑independent, useful for contracts.
  - Cons: needs trained analysts; subjective.
- **Story Points**: relative effort/complexity scale used in Agile.
  - Pros: team‑centric and flexible.
  - Cons: not comparable across teams.

### 2) Effort estimation
- Estimates **personnel requirements** and **man‑hours**.
- Often derived from size estimates (e.g., FP → effort model).

### 3) Time estimation
- Derived from effort + team capacity + schedule constraints.
- Use **Work Breakdown Structure (WBS)** to break work into manageable tasks for scheduling.

### 4) Cost estimation
- The hardest metric due to many influences:
  - hardware, licences, skilled personnel, travel, training.

## Standards and compliance (high level)
Know what these are associated with:
- Software Quality Assurance standard (SQA): **IEEE 730**
- Software Configuration Management (SCM): **IEEE 828**
- Verification & Validation (V&V): **IEEE 1012**
- Requirements specification process (SRS): **IEEE 29148**
- Software Project Management (SPM): **IEEE 16326**

## Common exam-style prompts
- Explain the Triple Constraint and what happens when one constraint changes.
- Given a scenario, identify which management activity is being described (risk management, reporting, etc.).
- Compare size measures (LOC vs FP vs Story Points): pros/cons and when they fit.
