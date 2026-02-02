# CSCS2102 — Lecture 3 Revision Notes
**Topic:** Functional & Non‑functional Requirements (FR/NFR)  
**Use with:** Quiz “lec3-quiz.html”

---
## 1) Requirements Engineering (RE)
- **Iterative loop:** **Elicitation → Specification → Validation**.
- **Risks:** Misunderstood **business/domain**, **cultural** gaps, vague statements, **moving target** (changing requirements).

**Moving target problem:** requirements change during development → **track changes** and manage impact.

---
## 2) Elicitation Techniques
- **Interviews** (semi‑structured), **Surveys** (broader sampling).
- Good questions: team‑coordinated, rehearsed, aimed at **resolving uncertainty** and **uncovering new needs**.

**Focused prioritisation prompt:** “Pick **two** for now, which **two** next?”

---
## 3) Capturing Requirements
- **User story template:** *As a* **[actor]**, *I want* **[action]**, *so that* **[rationale]**.
- **Actor:** person/device/entity that interacts with the system.
- Forms: **Natural language**, **Structured NL (user stories)**, **Pseudocode**, **UML** (class/use‑case/activity/sequence/state). Not Gantt.

---
## 4) FR vs NFR
- **Functional Requirements (FR):** *What* the system does — inputs/outputs, stored data, computations, reactions.
- **Non‑functional Requirements (NFR):** *How well* / constraints — **performance, reliability, usability, security, portability**, etc.
- **Blur case:** “Protect data from unauthorised access” (NFR intent) → login/authorisation (FR realisation).

---
## 5) Prioritisation — MoSCoW
- **Must‑Have:** vital to current delivery.  
- **Should‑Have:** important, high impact but not vital now.  
- **Could‑Have:** desirable, minor impact if omitted.  
- **Won’t‑Have (now):** out of current scope.

---
## 6) Make NFRs Measurable
Specify **Property + Metric + Operating conditions + Threshold**. Validate typically at **system testing**.

### Examples
- **Performance:** “p95 response ≤ **300 ms** at **500 RPS** (peak); throughput **≥ 100 TPS**.”
- **Reliability:** “Defect rate **< 1 failure / 1,000 hours**; availability **≥ 99.9%**.”
- **Usability:** “≥ **4/5** users complete Task X **≤ 5 min** after **2‑hour** training.”
- **Security:** “Time/resources to penetration ≥ **N**; ≤ **M** successful penetrations/year.”

**Limit vs Stress:** define normal operating limits and behaviour beyond them.

---
## 7) Security & Performance Testing (from slides)
- **Security methods:** **Fuzzing**, **SQL injection testing**, **Port scanning**, **Pen‑testing**.
- **Performance tests:** throughput/latency with explicit workloads, environments, and pass/fail **thresholds**.

---
## 8) Worked Examples
- **Clinic FR:** “User can **search appointment lists for all clinics**.”
- **Usability metric:** “4/5 users book in ≤ 5 minutes after 2‑hour intro.”

---
## 9) Trade‑offs & Rationale
- Provide **rationale** for numbers; surface **trade‑offs** (e.g., latency vs cost vs security).  
- **Rank priorities**; don’t hide uncertainty — refine values iteratively.

---
## 10) Common Pitfalls
- Vague adjectives: “fast”, “secure”, “user‑friendly”.  
- Non‑verifiable statements.  
- No operating conditions; tests impossible to pass/fail.

---
## 11) Quick Checks (self‑test)
- Distinguish **FR** vs **NFR** for three sample statements.  
- Write a measurable NFR with **property, metric, conditions, threshold**.  
- Pick **MoSCoW** priorities for five sample backlog items.  
- List **four** security testing methods.

---
## 12) Mini Glossary
- **Elicitation:** discovering requirements from stakeholders/sources.  
- **Specification:** documenting requirements precisely.  
- **Validation:** confirming requirements are correct/complete/testable.  
- **Actor:** entity (human/system/device) interacting with the system.
