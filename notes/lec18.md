# Topic 8 — Software Testing

## Overview
Software testing is the practice of checking software behavior so problems can be found before release and confidence can be built that the system meets its requirements.

The lecture frames testing as part of the broader **verification and validation** process.

---

## Why testing is needed
Testing matters because software faults can cause serious real-world failures.

The lecture uses the **Ariane 5 rocket launch failure** as an example:
- a software error in the inertial reference system contributed to failure
- a **64-bit floating-point number** was converted into a **16-bit signed integer**

Takeaway:
- software errors are not just theoretical
- defects can have major operational and safety consequences

---

## Core terminology

### Test case
A **test case** is a description of:
- a set of actions performed on software
- the expected outcome

### Test
A **test** is the execution of a test case, producing a test outcome.

### Testing
**Testing** is the practice of:
- creating test cases
- maintaining test cases
- executing test cases
- evaluating results

---

## Software testing definition and goals

### ITIL-style view from the lecture
Software testing is described as:
- a process to execute a program using data to simulate user inputs
- a process of locating or identifying errors / bugs before delivery to end users

### Main goals of testing
- demonstrate to stakeholders that software meets its requirements
- discover behavior that is:
  - incorrect
  - undesirable
  - not conforming to specification

This second goal is often referred to as **defect testing**.

---

## What makes a good test?
A good test:
- has a high probability of finding an error
- is neither too simple nor too complex
- is not redundant
- detects as many errors as possible

A useful way to think about it:
- a test should be focused enough to be meaningful
- but broad enough to reveal real faults

---

## Cost of errors over the life cycle
The lecture notes that:
- about **50%** of total SDLC effort and time may be spent on testing
- the sooner an error is found and corrected, the lower the cost
- costs may rise **exponentially** the later the error is discovered

Implication:
- catching defects early is much cheaper than fixing them after release or during operations

---

## Verification, validation, and defect testing

### Verification
Verification checks the **consistency of output with inputs**.

Key question:
- **Are we building the product right?**

Typical characteristics:
- happens earlier
- focuses on architecture, design, specification
- uses static activities
- does **not** require executing code

Typical methods:
- reviews
- walkthroughs
- inspections

### Validation
Validation assesses how well software **fulfills requirements and meets users' needs**.

Key question:
- **Are we building the right product?**

Typical characteristics:
- happens after verification
- focuses on the actual product
- uses dynamic activities
- **does** involve code execution

Typical methods:
- black-box testing
- white-box testing
- non-functional testing

### Defect testing
Defect testing focuses on finding faults where the software behavior is incorrect or does not match its specification.

---

## Inspections vs testing

### Inspections
Inspections are concerned with analyzing **static system representations** to discover problems.
Examples of things that may be inspected:
- requirements specification
- software architecture
- UML design models
- database schemas
- program code

### Testing
Testing is concerned with **exercising and observing product behavior**.

### Relationship between them
Inspections and testing are:
- **complementary**
- not alternatives where one fully replaces the other

Important limitation:
- inspections can check conformance with specifications
- inspections **cannot** properly check non-functional characteristics such as:
  - performance
  - usability

---

## Strategies for evaluating software
The lecture groups evaluation strategies into four types.

### 1) Static manual
- program inspection
- example: another programmer checks the code manually

### 2) Static automatic
- program analysis
- example: a tool checks code for common errors or bad practice

### 3) Dynamic manual
- testing
- example: a person runs tests to check software behavior

### 4) Dynamic automatic
- runtime checking
- example: the software automatically detects bad states during operation

---

## Static testing vs dynamic testing

### Static testing
- helps find bugs **without executing code**
- used during verification
- generally more cost-effective
- examples:
  - review
  - walkthrough
  - inspection

### Dynamic testing
- requires **execution of code**
- used during validation
- generally more expensive than static testing
- examples:
  - unit testing
  - integration testing
  - system testing

---

## Stages of testing
The lecture gives three broad stages.

### 1) Development testing
Testing done during development to discover bugs and defects.

### 2) Release testing
A **separate testing team** tests the complete software before release.

### 3) User testing
Users or potential users test the software in their own environment.

Expected finding across these stages:
- actual behavior does not match expected behavior

---

## Development testing levels

### Unit testing
Tests:
- individual units
- individual classes
- specific functions or methods

Purpose:
- check correctness of small parts where expected answers are known

Simple example idea:
- call a function with known inputs
- compare the output with the expected result

### Integration testing
Tests whether several individual units work correctly **together** as composite components.

### System testing
Tests some or all integrated parts of the system **as a whole**.

---

## Error-handling approaches
When an error occurs at runtime, the lecture describes three common approaches.

### 1) Ignore
- error is ignored
- program continues running

### 2) Fail fast
- program stops immediately
- error is reported

### 3) Fail safe
- program acknowledges the error
- continues execution in the best possible way

### General principle from the lecture
In general, software should **fail fast** because continuing execution after an error can be risky and may cause more serious damage.

---

## Black-box, white-box, and gray-box testing

### Black-box testing
Also called **functional testing**.

Characteristics:
- based on analysis of requirements
- tests what happens at the interface
- testers do **not** need to know the internal structure of the code
- can be applied at unit, integration, system, and acceptance levels

### White-box testing
Also called **structural testing**.

Characteristics:
- based on internal logic, design, and code
- compares actual behavior with expected results

### Gray-box testing
Characteristics:
- look at the code to design test cases
- execute the test through the interface

---

## Black-box input distribution ideas
The lecture shows that input selection matters.

### Ideal case
A good distribution of inputs helps achieve a good distribution of code being tested.

### Sufficient tests idea
A small range of inputs may exercise a small but important and error-prone region of code.

### Unnecessary tests problem
A large range of inputs may still exercise only a small part of the code.

Meaning:
- many tests do not automatically mean good coverage

### Insufficient tests problem
A small range of inputs may exercise a large range of code, but it may still miss:
- some parts
- edge cases
- extremes

Meaning:
- coverage must be judged carefully, not just by the number of tests

---

## Quick comparison table

| Concept | Main idea |
|---|---|
| Verification | Are we building the product right? |
| Validation | Are we building the right product? |
| Inspection | Static analysis of artifacts |
| Testing | Dynamic observation of software behavior |
| Static testing | No code execution |
| Dynamic testing | Code execution required |
| Black-box testing | Requirement / interface focused |
| White-box testing | Internal logic / code focused |
| Gray-box testing | Code-informed design, interface-based execution |

---

## Revision checklist
Make sure you can explain:
- why software testing is needed
- Ariane 5 example
- test case vs test vs testing
- goals of software testing
- features of a good test
- why earlier bug discovery reduces cost
- verification vs validation
- inspections vs testing
- static manual / static automatic / dynamic manual / dynamic automatic
- static vs dynamic testing
- development testing, release testing, user testing
- unit, integration, and system testing
- ignore vs fail fast vs fail safe
- black-box vs white-box vs gray-box testing
- why poor input selection can lead to unnecessary or insufficient tests
