# Topic 3 — Quality Assurance, Code Review & Software Metrics (Revision Notes)

## Quality concepts
### Quality Assurance (QA)
- **Systematic efforts** to ensure products meet expectations: performance, design, reliability, maintainability.
- Core aim: **prevent** mistakes and defects.

### Quality Control (QC)
- Focuses on **detecting** defects (inspection/testing after creation).

### ISO 9000 view (high level)
- QA is part of quality management that provides confidence that quality requirements will be fulfilled.
- ISO 9001 commonly applies to organisations involved in design/development/production/servicing (typical software org fit).

## Code review
### Definition
- A methodical assessment of code to identify bugs, improve quality, and help developers learn the codebase.

### Typical process expectations
- Every commit reviewed by at least one other developer using integrated tools.
- Reviews linked to a system of record (e.g., issue tracker).
- Feedback should be:
  - constructive,
  - objective (explain “why”),
  - focused on standards, security, and best practices.

### Benefits
- Improved software quality.
- Knowledge sharing and mentoring.
- Increased collaboration and standard adherence.
- Cheaper than fixing defects after release.

### Common obstacles
- Workload, deadlines/time constraints, lack of manpower.

## Best practices for high-quality code (review checklist themes)
### Review guidelines
- Use **checklists**: readability, security, test coverage, architecture, reusability.
- Limit review volume:
  - Recommended: **200–400 LOC** per review chunk.
  - Larger chunks reduce defect detection rate.

### Clean code techniques
- Prefer direct returns for boolean conditions instead of verbose if/else.
- Avoid unnecessary temporary variables; return expressions/objects directly when clear.
- Naming:
  - avoid abbreviations,
  - choose descriptive function/variable names,
  - follow consistent casing conventions.
- Avoid “clever” complex one‑liners that reduce readability.
- Reduce nesting; use guard clauses to keep the “happy path” clear.
- Encapsulate repeated logic into functions for reuse.
- Choose appropriate data structures (e.g., set for uniqueness).

## Measurement and metrics
- No single metric fits all teams; mature teams combine size, effort, complexity, productivity.

### Size / effort examples (from metrics table)
- **LOC**: simple but language‑dependent and may encourage verbosity.
- **Function Points**: language‑independent but subjective and needs trained analysts.
- **Story Points**: team‑centric but not comparable across teams.
- **COCOMO**: predictive model using size and cost drivers; needs calibration and can be less accurate for Agile.
- **Cycle/Lead time**: customer-focused; highlights bottlenecks but not complexity.

## Code review metrics
- **Inspection rate** = LOC / inspection hours
  - Too slow can indicate readability issues.
- **Defect rate** = defects found / inspection hours
  - Helps estimate review/testing effectiveness.
- **Defect density** = defects / KLOC
  - Helps locate vulnerable components needing resources.

## Cyclomatic Complexity (CC)
### What it measures
- Logical complexity: number of **independent execution paths** through code.

### How to calculate
- Graph-based: V(G) = E − N + 2P (control flow graph).
- Shortcut for a single function:
  - **CC = number of decision points + 1**

### Decision points (typical examples)
- if, else-if, switch/case branches, loops, conditional operators, and similar branching constructs.

## Professor revision-style prompt patterns
- Given a code snippet, compute CC using decision points + 1.
- Explain QA vs QC and why prevention matters.
- Choose the best metric for a given goal (productivity, complexity, bottlenecks).
- Identify why large reviews reduce effectiveness and how to fix (split by LOC, checklist, etc.).
