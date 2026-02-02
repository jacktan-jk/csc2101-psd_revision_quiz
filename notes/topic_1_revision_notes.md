# CSCS2102 — Topic 1 Revision Notes
**Topic:** Introduction to Software Engineering (SE) & Process  
**Use with:** Quiz “topic_1_quiz.html”

---
## 1) What is Software Engineering?
- **Discipline** focused on producing **high‑quality software**, **on time**, **within budget**, that **satisfies user needs**.
- Goes beyond coding: includes **documentation, libraries, support sites, configuration data**.

### Why SE matters
- Common failures: **over budget**, **late**, **unreliable**, **doesn’t meet requirements**, **hard to maintain**, **poor performance**, or **never delivered**.

---
## 2) “Good” Software — Core Product Qualities
- **Functionality**: does what users need.
- **Dependability & Security**: safe failure modes; prevents malicious access/damage.
- **Usability**: easy to learn and operate.
- **Efficiency**: time, memory, responsiveness, power.
- **Maintainability**: easy to fix, extend, and adapt.

> Practical tip: Treat **quality attributes** as **requirements**; make them **measurable** (e.g., “p95 response < 300 ms at 500 RPS”).

---
## 3) Software Engineering Layers
- **Process** (foundation): governs how work is done across the lifecycle.
- **Methods**: analysis, design, modelling, verification.
- **Tools**: CASE tools, IDEs, CI/CD, issue trackers.
- **Quality focus** overlays every layer.

---
## 4) Software Development Life Cycle (SDLC)
1. **Requirement Specification** – capture WHAT the system should do.
2. **Analysis & Design** – transform requirements into a solution approach.
3. **Implementation** – build the software.
4. **Testing** – verify against requirements (unit → system).
5. **Deployment** – deliver to users.
6. **Maintenance** – fix/modify post‑release.

**Cost reality:** Over a product’s lifetime, **maintenance dominates** total cost.

---
## 5) Process Models — When to Use What
### Waterfall (sequential)
- **Use when:** requirements are **well‑defined**, resources adequate, team experienced, product **not too large/complex**, no urgent partial delivery.
- **Pros:** simple planning, clear milestones, strong documentation.
- **Cons:** brittle to change; late validation.

### Incremental (core → increments)
- Start with **core product** (basic needs), then add features by **priority**.
- **Use when:** need **quick limited functionality**, some details will change, **new tech**, or team still maturing.
- **Note:** different increments may use **different internal models**.

### Evolutionary (iterative + incremental)
- Family of approaches that **embrace change over time**.
- Examples: **Prototyping**, **Spiral**.

#### Prototyping
- **Use when:** **unclear/incomplete requirements**, **small/low‑cost** systems, strong **customer involvement**, team lacks expertise.
- Build throw‑away or evolutionary prototypes to refine needs.

#### Spiral (risk‑driven)
- **Use when:** **high‑risk**, **large/complex** projects, **unclear requirements**, need **frequent releases**.
- Cycles: objectives → risk analysis → development → evaluation.

### Plan‑Driven vs Agile
- **Plan‑Driven:** upfront requirements/design, heavier documentation; fits stable domains, compliance contexts.
- **Agile:** **requirements & design evolve together**; small motivated teams; early/incremental delivery; high customer collaboration; simplicity.

> Hybrid is common: e.g., **Incremental overall**, **Waterfall within increments**, and **Prototyping** for the uncertain part.

---
## 6) Practical Patterns & Anti‑Patterns
**Do:**
- Keep a **repeatable process** across the full life‑cycle.
- Prioritise by **value/risk**, timebox work, demo early.
- Treat **quality attributes** as first‑class requirements.

**Avoid:**
- Big‑bang delivery with late testing.
- Ambiguous requirements (lack of user validation).
- Ignoring **maintenance** (docs, tests, observability).

---
## 7) Quick Checks (self‑test)
- Can you list the **five core qualities** of good software?
- What SDLC step comes **before** testing? What comes **after**?
- When would you **not** choose Waterfall?
- Give one project scenario best served by **Spiral**.
- Define a **core product** and why it matters.

---
## 8) Exam/Interview Flash Cards
- **SE vs Programming:** SE = product + process + quality + people; programming = coding.
- **Efficiency vs Performance:** efficiency includes **time + memory + responsiveness + power**.
- **Maintenance cost:** typically **> development** over lifetime.
- **Agile principle (in one line):** early, continuous delivery through collaboration and adaptation.

---
## 9) Mini Glossary
- **Requirement:** verifiable statement of needed capability or constraint.
- **Process Model:** structured approach to organising SDLC activities.
- **Prototype:** simplified implementation to explore requirements/risks.
- **Increment:** deployable subset that adds value.

---
## 10) Suggested Metrics Templates
- **Performance:** “p95 latency ≤ 300 ms at 500 RPS; throughput ≥ 100 TPS.”
- **Reliability:** “≤ 1 failure / 1,000 operating hours; availability ≥ 99.9%.”
- **Usability:** “≥ 4/5 users complete Task X ≤ 5 min after 2‑hour training.”
