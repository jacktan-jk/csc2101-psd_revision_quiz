# CSC2101 — Lecture 4 Revision Notes
**Topic:** UML Class Diagrams & Use Case Diagrams  
**Use with:** Quiz “lec4-quiz.html”

---
## 1) UML Modelling — Why & What
- **UML = graphical notation** to represent a system from different views.
- Two families:
  - **Structural models** — organisation/relationships of parts (e.g., **Class diagram**).
  - **Behavioural models** — dynamic responses to stimuli (e.g., **Use case**, Activity, Sequence, State).
- **Data‑driven vs Event‑driven**: data‑driven shows processing from input→output; event‑driven shows reactions to external/internal events.

---
## 2) Class Diagram — Core Elements
- **Class**: name, **attributes**, **operations**.
  - Visibility: `+` public, `#` protected, `-` private.
- **Associations**: semantic links between classes.
  - **Multiplicity** (cardinality) at each end:
    - `0..1` (optional), `1` (exactly one), `1..*` (one or more), `0..*` (many).
  - **Role names** (optional) clarify meaning of each end.
  - **Association attributes** are allowed (e.g., `Quantity` on `Order–Item`).
- **Aggregation/Composition (part–whole)**
  - **Aggregation** (hollow diamond): parts can exist independently of whole.
  - **Composition** (filled diamond): parts’ lifetime bound to whole.
- **Generalization (Inheritance)**
  - Triangle/arrow **points to the super‑class**; sub‑classes inherit attributes/operations.
- **Constraints**: express rules (OCL, notes, or text), e.g., _“Admin manages ≥ 10 Applications”_.

### Reading Multiplicity Quickly
- `1..*` → **at least** one.  
- `0..*` → **zero or many**.  
- `0..1` → optional single.  
- Exact `n` → precisely `n`.

### Example Patterns
- **Association class** when the **relationship itself has data** (e.g., `Enrollment` between `Student` and `Course`).
- **Many‑to‑many** becomes two one‑to‑many associations via an association class/table.

---
## 3) Use Case — Purpose & Scope
- **Definition:** A **collection of scenarios** describing interactions between the **system** and **external actors** to achieve a goal.
- **Actor:** person, device, or external system that **interacts with** (but is **outside**) the system boundary.
- Diagram conveys **“who does what”** at a glance; detailed steps live in the **use case specification**.

### Diagram Notation
- **Actors**: stick‑person (human) or rectangle (non‑human actor), outside the system.
- **Use cases**: ellipses **inside** the system boundary (box).
- **Relationships:**
  - **Include** `<<include>>` — base use case **always** calls included one (reuse mandatory behaviour).
  - **Extend** `<<extend>>` — extension adds behaviour to base **under conditions** (optional/variant flow).
  - **Generalization** — an actor or use case **specialises** another.

### Use Case Template (Short)
- **Primary actor**  
- **Goal in context**  
- **Preconditions**  
- **Trigger**  
- **Main success scenario** (numbered steps)  
- **Extensions** (alternates/exceptions)  
- **Postconditions**  
- *(Extended template may add: priority, availability, frequency, channels, secondary actors, open issues.)*

#### Mini Example — Home Security System
- **Actors:** Homeowner, IT Technician, Sensors (non‑human).  
- **Use cases:** *Arm/Disarm*, *Remote Access*, *Respond to Alarms*, *Reconfigure Sensors & Features*, *Encounter Errors* (extensions).  
- **Notes:** Non‑human actors shown as rectangles; conditional flows via **extend**.

---
## 4) Common Mistakes to Avoid
- Mixing **detailed scenarios** into **class diagrams** (keep those in use case specs/activity/sequence).
- Omitting **multiplicity** → ambiguous designs.
- Wrong direction of **generalization arrow** (must point to **super‑class**).
- Using **include** when the behaviour is optional (should be **extend**).
- Modelling only humans as actors — devices/systems can be actors too.

---
## 5) Quick Design Checklist
**Class Diagram**
- [ ] Classes named with clear responsibilities.  
- [ ] Associations labelled; **multiplicities** on both ends.  
- [ ] Part–whole as **aggregation/composition** where appropriate.  
- [ ] Inheritance only for true **is‑a** relationships; avoid misuse for code reuse.  
- [ ] Constraints captured (notes/OCL).

**Use Case Diagram & Spec**
- [ ] System boundary drawn; actors outside.  
- [ ] **Include** for mandatory sub‑behaviours; **extend** for optional/conditional.  
- [ ] Concise spec: preconditions, trigger, **main flow**, **extensions**, postconditions.  
- [ ] Link each use case to **supporting scenarios** (activity/sequence).

---
## 6) Quick Checks (self‑test)
- Interpret `0..*` vs `1..*` vs `0..1`.  
- Choose **include** or **extend** for a given situation.  
- Where does the **generalization** arrow point?  
- When would you model an **association class**?  
- Name two **non‑human** actors you might show.

---
## 7) Mini Glossary
- **Association:** relationship between classes with optional **multiplicity** & role names.
- **Aggregation/Composition:** whole–part; composition ties part lifetime to whole.
- **Generalization:** inheritance (specialisation).
- **Use Case:** goal‑oriented interaction between actor and system.
- **Include/Extend:** mandatory reuse vs conditional extension of behaviour.
