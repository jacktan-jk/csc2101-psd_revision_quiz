# Topic 9 — Configuration Management

## Overview
Configuration Management (CM) is about keeping a product consistent with its requirements, design, and operational information across its whole life.

The lecture presents CM as a disciplined way to manage change, maintain control, and preserve traceability as systems evolve.

---

## What configuration management means
Configuration management is defined as a process used to establish and maintain the consistency of a product's:
- performance attributes
- functional attributes
- physical attributes

These must stay aligned with:
- requirements
- design
- operational information

### Historical context
The lecture notes that CM was widely used in **military engineering**, especially for complex systems such as:
- weapon systems
- military vehicles
- information systems

Outside the military, similar ideas are also used in:
- IT service management
- civil engineering
- other engineering domains

---

## Software Configuration Management (SCM)
Software Configuration Management applies CM ideas to software projects.

According to the lecture, SCM is treated by practitioners as one of the best ways to handle change in software development.

### What SCM does
SCM:
- identifies software attributes at different points in time
- controls changes systematically
- supports integrity and traceability across the SDLC
- helps verify that a release contains the planned enhancements

### Why SCM matters
Without control over versions, changes, and release contents, it becomes difficult to:
- know what changed
- know why it changed
- verify what is included in a release
- maintain confidence in the delivered product

---

## The 4 core SCM procedures
The lecture identifies four procedures that should be defined for each software project:

1. **Configuration identification**  
   Define what items are being controlled.

2. **Configuration control**  
   Manage and approve changes systematically.

3. **Configuration status accounting**  
   Record and report the current status of configuration items and changes.

4. **Configuration audits**  
   Verify that configuration information and changes are correct and complete.

A good exam memory aid:
- identify
- control
- account
- audit

---

## Services and ITILv3
The lecture connects configuration management to **ITILv3**.

### Service definition
A service is described as:
- a means of delivering value to customers
- by helping them achieve outcomes they want
- without them owning the specific costs and risks

### Configuration management in ITILv3
In ITILv3, configuration management is responsible for maintaining information about:
- configuration items (CIs) needed to deliver an IT service
- the relationships between those items

This information is managed across the whole lifecycle of the CI.

The lecture also states that configuration management is part of the broader:
**Service Asset and Configuration Management** process.

### Discussion prompt from the lecture
The slides raise reflection questions such as:
- Is software a service?
- How has that answer changed over time?
- Which framework is more suitable in context: PMP, PRINCE2, or ITIL?

These are presented as discussion prompts rather than fixed answers.

---

## Assets vs configuration items (CIs)

### Asset
An **asset** is something with intrinsic value to a person or an enterprise.

### Configuration Item (CI)
A **configuration item** is an entity or thing that needs to be tracked or monitored in order to deliver a service.

### Important rule
The lecture gives this rule of thumb:
- an asset is often a CI
- but a CI is not necessarily an asset

---

## Server example: asset vs CI
The lecture uses a **server** to show the distinction.

### As an asset
Typical asset-style attributes include:
- model
- CPU
- RAM
- OS

### As a CI
The CI view includes:
- technical details
- ownership details
- relationship details

#### Ownership examples
- responsible person
- purchase date
- warranty information
- location

#### Relationship examples
How the server contributes to service delivery and, ultimately, business value.

---

## The Configuration Management Database (CMDB)
A **CMDB** is a file or, more commonly, a standardized database that contains relevant configuration information.

It stores information about:
- hardware components
- software components
- relationships between components

### Why a CMDB is useful
The lecture says a CMDB provides:
- an organized view of configuration data
- a way to examine that data from different perspectives

In practice, this supports better visibility and control.

---

## What counts as a CI
The lecture emphasizes that CIs are the focal point of a CMDB.

A CI should be:
- a direct part of the environment
- an instance of an entity
- configurable, with attributes specific to that instance

### Examples of CIs
The lecture gives examples across different categories:

#### Physical
- computer systems
- buildings

#### Logical
- installed instances of software

#### Conceptual
- business services
- employees

---

## What does not count as a CI

### Incident ticket
Not a CI because it is **information about** another entity, not a direct part of the environment.

### Generic software package
Not usually treated as a CI in this context because the package itself is not the deployed instance in the environment.  
Only the **installed instance** is treated as a CI.  
The generic package is usually stored in the **Definitive Media Library (DML)**.

### Event
Not a CI because it does not have configurable attributes and is not part of the environment.

---

## CI eligibility matrix
The lecture recommends using a **CI eligibility matrix** to decide which items in an IT environment should be tracked as CIs.

### What it contains
A CI eligibility matrix lists:
- the CI candidate
- its CI type
- the criteria used to decide whether it should be a CI

### Example criteria from the lecture
- **Cost or value**  
  Does it have business value or monetary value?

- **Change considerations**  
  Would it be affected by change requests?

- **Traceability**  
  Do you need to track changes made to it?

- **Governance and compliance**  
  Is it important for standards or compliance requirements?

- **Management of service commitments**  
  Is it needed to meet service obligations?

- **Maintainability**  
  Are you required to maintain it?

- **Delivery cost and quality**  
  Is there a cost related to delivery and maintenance?

- **Other business-specific factors**  
  For example:
  - do you manage it rather than a third party?
  - is it unique?

### Key takeaway
Not every item should automatically become a CI.  
The CI eligibility matrix helps make that decision systematically.

---

## Consumer protections, warranty, and maintenance
The later part of the lecture connects configuration and asset thinking to support and protection concepts.

### Magnuson-Moss Warranty Act
The lecture mentions this US law as a consumer protection statute for warranties.

Key point:
- products do **not** have to be sold with a warranty
- but if a warranty is offered, it must comply with the law

The lecture notes that this was meant to prevent unfair or misleading warranty disclaimers.

### Maintenance vs warranty
This distinction is exam-relevant:

#### Maintenance
- routine service
- usually paid out of pocket by the owner

#### Warranty
- a guarantee to fix the asset
- applies when major damage occurs or the asset does not perform as expected

---

## Extended warranty example
The lecture cites a **Consumer Reports** survey on laptop extended warranties.

The summary given is:
- extended warranties are probably **not worth the investment**
- among surveyed PC owners with extra coverage, only **15%** used it for repairs
- among Apple owners with extra coverage, only **7%** used it

This is presented as an example of how warranty decisions can differ from routine maintenance needs.

---

## Exam-focused recap

### Know these definitions
- configuration management
- software configuration management
- service
- asset
- configuration item
- CMDB
- maintenance
- warranty

### Memorize these four SCM procedures
- configuration identification
- configuration control
- configuration status accounting
- configuration audits

### Be able to explain
- the difference between an asset and a CI
- why a CMDB matters
- why incident tickets and generic software packages are not CIs
- how a CI eligibility matrix helps decide what should be tracked
- the difference between maintenance and warranty

### Fast memory hooks
- **CM** = consistency through change
- **SCM** = control + traceability for software
- **CI** = track it because service delivery depends on it
- **CMDB** = where CI data and relationships are organized
- **Warranty** = guarantee
- **Maintenance** = routine upkeep
