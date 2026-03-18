# Topic 5 — Maintenance and Documentation

## Overview
Software is not static. It needs ongoing maintenance and supporting documentation so it remains reliable, secure, useful, and easier to evolve over time.

## Why Maintenance and Documentation Matter

### 1. Bug fixing and issue resolution
Software can contain defects that affect:
- functionality
- performance
- security

Maintenance is needed to identify the issue, diagnose it, fix it, test the fix, and deploy the updated version.

### 2. Software updates and upgrades
Software changes over time. Maintenance supports:
- new features
- performance improvements
- vulnerability fixes
- continued relevance to users and the business

### 3. User support and training
Documentation helps users:
- understand what the system does
- learn how to use it properly
- troubleshoot common issues
- use features more effectively

Examples include:
- user manuals
- help files
- training materials

### 4. Codebase maintenance
A codebase becomes harder to work with over time if it is not maintained. Maintenance work includes:
- refactoring
- optimization
- improving maintainability
- keeping the code organized and efficient

---

## The Danger of Poor Documentation
The lecture uses **Varig Flight 254 (1989)** as an example of how poor documentation can contribute to real-world harm.

Key point:
- The accident involved a combination of pilot error, inadequate training, and lack of proper documentation for the aircraft's navigation system.

Takeaway:
- Documentation is not just paperwork. Poor documentation can cause misunderstanding, incorrect operation, and serious consequences.

---

## Responsibility for Fixing Issues
Whether it is your responsibility to fix a software issue depends on several factors.

### Role
- If you are a developer of the software, fixing related issues is likely your responsibility.
- If you are a normal user, it is usually not your responsibility to fix the problem, although reporting it is still useful.

### Level of authority
- If you have permission or authority to modify the software or codebase, it may fall under your responsibility.

### Nature of the issue
- **Bug or defect in software** → usually the development team's responsibility
- **User behavior error or hardware problem** → usually not the development team's responsibility

---

## The 5 Types of Software Maintenance

### 1. Corrective maintenance
**Definition:** Fixing defects or bugs to restore correct system behavior.

**Goal:** Get the software back into a correct working state.

**Typical activities:**
- identify the bug
- diagnose the root cause
- implement a fix
- test the fix
- deploy the fix

**Example:** A mobile payment app fails to complete transactions because of a code defect.

---

### 2. Adaptive maintenance
**Definition:** Modifying software to meet changing user or business requirements.

**Goal:** Keep the software relevant over time.

**Typical changes:**
- features
- user interface
- performance behavior
- data model changes required by new business needs

**Example:** An inventory system is updated to support multiple languages and currencies after international expansion.

---

### 3. Perfective maintenance
**Definition:** Improving the software's functionality, performance, or overall quality.

**Goal:** Enhance capability and quality.

**Typical improvements:**
- speed
- efficiency
- usability
- new useful features

**Example 1:** Optimizing a slow order and inventory application  
**Example 2:** Adding a reporting module  
**Example 3:** Adding two-factor authentication

---

### 4. Preventive maintenance
**Definition:** Proactively identifying and fixing potential problems before they become real failures.

**Goal:** Reduce the risk of failure and improve long-term reliability.

**Typical activities:**
- regular backups
- log monitoring
- security audits
- penetration testing
- implementing security best practices

**Example:** A cloud-based financial application is hardened with encryption, access controls, firewalls, and regular security testing.

---

### 5. Emergency maintenance
**Definition:** Fixing critical issues as fast as possible.

**Goal:** Minimize downtime and restore service quickly.

**Typical situations:**
- system crashes
- security breaches
- urgent production incidents

**Example:** A mission-critical airline application crashes and blocks access to flight data, so the team rolls back changes and applies a temporary fix immediately.

---

## Why This Classification Matters
Understanding maintenance categories helps software engineers:
- prioritize work
- choose the right response
- plan better maintenance strategies
- keep software reliable, functional, and relevant over time

---

## README
A **README** is a project file that explains:
- what the project is
- its purpose
- how to install it
- how to use it

### Important rule
A README is **not** meant to be a deep technical explanation of how the source code is programmed.

Its purpose is to help users understand and use the project.

---

## README Best Practices

### Keep it concise
- include the important information
- avoid unnecessary long descriptions

### Use clear language
- write simply
- avoid jargon where possible
- make it understandable even for non-technical users

### Provide an overview
Start with a short explanation of:
- project purpose
- major features
- target audience

### Explain installation and usage
Include:
- prerequisites
- setup steps
- configuration details
- instructions for running or using the software

### Include examples
Examples make the README easier to follow, such as:
- screenshots
- sample commands
- code snippets
- typical usage scenarios

### Provide contact information
Include a way for users to get help or report issues, such as:
- email address
- support forum link

### Update regularly
Keep the README aligned with the current software so users are not misled by outdated instructions.

---

## Quick Classification Guide

| Scenario | Maintenance Type |
|---|---|
| Fixing a bug that causes a crash | Corrective |
| Updating software for new business or user requirements | Adaptive |
| Improving speed, usability, or adding valuable features | Perfective |
| Auditing and fixing potential weaknesses before failure | Preventive |
| Restoring service during a critical outage | Emergency |

---

## Quick Revision Points
- Maintenance is needed because software changes, breaks, and grows over time.
- Documentation supports users and reduces misuse and confusion.
- Poor documentation can contribute to serious real-world failures.
- Responsibility depends on role, authority, and issue type.
- The five maintenance types are:
  1. Corrective
  2. Adaptive
  3. Perfective
  4. Preventive
  5. Emergency
- A README explains the project and how to use it, not the internal code design.
