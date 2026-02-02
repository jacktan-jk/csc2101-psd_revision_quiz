# CSCS2102 — Topic 5 Revision Notes
**Topic:** UML Behavioural Modelling & Software Reuse  
**Use with:** Quiz “topic_5_quiz.html”

---
## 1) Behavioural Modelling Overview
Goal: capture **how the system behaves over time** and in response to **events**. Key diagrams:
- **Activity Diagram** — procedural **flow of actions** (what happens). Good for elaborating a **use case scenario**.
- **Sequence Diagram** — **time‑ordered collaboration** between objects (who talks to whom, when).
- **State Machine (Statechart)** — **event‑driven** behaviour across **states** and **transitions**.

> Pipeline: requirements → use cases → activity/sequence/state diagrams → design.

---
## 2) Activity Diagrams — Quick Reference
- **Use for:** workflow, business logic, algorithm steps, happy/alternate paths.
- **Symbols:**
  - **Action** (rounded rectangle)
  - **Decision/Merge** (diamond) — guards label outgoing edges
  - **Fork/Join** (thick bars) — parallelism & synchronisation
  - **Start/End** (filled circle / bull’s‑eye)
  - **Swimlanes (optional):** partition by responsible party
- **Notes:** focus on **what** happens; actor identity is secondary (use lanes if needed).

---
## 3) Sequence Diagrams — Quick Reference
- **Use for:** depict **objects + messages over time** for one scenario.
- **Key elements:**
  - **Actor/Object lifeline** (vertical dashed line) with **activation** bars
  - **Messages:** synchronous, asynchronous; return arrows; self‑call (reflexive)
  - **Creation/Deletion** of objects (lifecycle messages)
- **Tips:** start the sequence from an **external actor** or another object; keep focus on **message order**.

---
## 4) State Machines — Quick Reference
- **Use for:** systems with **modes** and **events** (e.g., devices, protocols, UI states).
- **Elements:** **States**, **Events** (triggers), **Transitions**, **Actions** (effects), **Guards** (conditions), **Composite states** (nesting).
- **Example — Microwave:** states include *Waiting, Half power, Full power, Set time, Disabled, Enabled, Operation*; events: *Number, Timer, Door open/closed, Start, Cancel*.
- **Rule of thumb:** specify **what must not happen** (e.g., *must not operate with door open*).

---
## 5) Software Reuse — Concepts
- **Component:** self‑contained bundle of **state + behaviour** with **well‑defined interfaces**.
  - **Provided interfaces:** services it **offers**.
  - **Required interfaces:** services it **needs** from others.
- **Levels of reuse:** **System**, **Application**, **Component**, **Object/Function**.
- **General‑purpose vs Application‑specific:** common functionality for many apps **vs** domain‑specific logic.

### Benefits (from slides)
- Higher **reliability**, **faster delivery**, **reduced process risk**, better use of specialists, standards compliance.

### Problems/Costs
- Tooling gaps; effort to **understand/adapt/integrate**; **maintenance** burden; library costs; **Not‑Invented‑Here** syndrome.

### Example — Print Service Component
- **Provided ops:** *Register/Unregister, GetQueue, Remove, Transfer*.
- **Design rule:** clear **responsibilities**, interfaces minimise coupling; dependencies expressed via **required interfaces**.

---
## 6) Choosing the Right Diagram
- **Elaborate steps inside one use case?** → **Activity**
- **Time‑ordered collaboration across objects?** → **Sequence**
- **Event‑driven mode changes and reactions?** → **State**

---
## 7) Mini Patterns & Anti‑patterns
**Patterns**
- Merge many‑to‑many interactions into an **intermediary** (controller/mediator) to simplify sequences.
- Use **fork/join** for parallel flows instead of tangled decision trees.
- Encapsulate volatile integrations behind **required interfaces**.

**Anti‑patterns**
- Overusing **include/extend** in behaviour diagrams (those belong to **use case** models).
- Sequence diagrams that turn into **class dumps** (keep them scenario‑centric).
- State machines with **event names as states** (state ≠ event).

---
## 8) Checklists
**Activity**
- [ ] Clear start/end; decisions with **guards**.  
- [ ] Parallel branches with explicit **fork/join**.  
- [ ] Map steps to **use case** flow.

**Sequence**
- [ ] Identify participating **actors/objects**.  
- [ ] Messages ordered; returns shown where useful.  
- [ ] Lifetimes/activations make sense; self‑calls marked.

**State**
- [ ] States are **modes**; events/guards trigger **transitions**.  
- [ ] Actions clearly defined; **forbidden behaviours** captured.  
- [ ] Composite states used to manage complexity.

**Reuse**
- [ ] Provided/required interfaces documented.  
- [ ] Dependencies minimal and explicit.  
- [ ] Reuse level chosen deliberately (system/app/component/object).

---
## 9) Quick Checks (self‑test)
- Which diagram best suits **PAY‑BILL** step‑by‑step flow? Why?
- In a sequence diagram, what does the **lifeline** represent?
- Give two **events** and two **states** for the microwave example.
- Name **two benefits** and **two challenges** of reuse.
- Differentiate **provided** vs **required** interfaces.

---
## 10) Mini Glossary
- **Action:** atomic step in an activity diagram.
- **Guard:** Boolean condition on a transition/edge.
- **Lifeline:** temporal existence of an object/actor in a sequence diagram.
- **Composite State:** state that contains substates.
- **Component:** deployable unit with provided/required interfaces.
