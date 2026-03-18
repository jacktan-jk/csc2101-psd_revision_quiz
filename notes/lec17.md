# Topic 6 — Deployment

## Topic
Deployment

## What is software deployment?
Software deployment is the set of activities that make a software system available for use.  
There is no single exact procedure for every system, because each system has different requirements and characteristics.

## Core deployment activities

### 1) Release
Release is the preparation work done after development is completed.
It includes:
- preparing the system for assembly and transfer to the target computer systems
- determining resources needed for acceptable performance
- planning or documenting later deployment steps

### 2) Installation
Installation sets up the software so it can run.
For simple systems, this may mean:
- a command
- a shortcut
- a script
- a service

For complex systems, installation may also involve:
- configuration
- asking users how the system should be configured
- preparing required subsystems

### 3) Activation
Activation means starting the executable component for the first time.

### 4) Deactivation
Deactivation is the opposite of activation.
It means shutting down running components.

Why it matters:
- often needed before updates
- may be part of system retirement / decommissioning

### 5) Uninstallation
Uninstallation is the opposite of installation.
It removes a system that is no longer needed.

It may also require:
- reconfiguring other software
- removing dependencies on the uninstalled system

### 6) Update
An update replaces an older version of all or part of the system with a newer release.

Typical flow:
1. deactivate
2. install updated version

Some software has built-in update mechanisms.
These can range from:
- fully automatic
- user-initiated and user-controlled

---

## Deployment environments

### Local
Developer's own workstation.

### Development / Trunk
Sandbox environment for developer unit testing.

### Integration
Often the CI build target.
Used for testing side effects across the system.

### Testing / Test / QC / Internal Acceptance
Used for interface testing and quality control.
Goal:
- verify that new code does not break existing functionality
- test major features after deployment to the test environment

### Staging / Stage / Model / Pre-production / External-Client Acceptance / Demo
A mirror of production.

### Production / Live
Environment that serves real end-users or clients.

---

## Deployment architectures

### DTAP
DTAP stands for:
- Development
- Testing
- Acceptance
- Production

It is a phased approach to software testing and deployment.

### Other variants
The lecture also mentions possible extensions such as:
- **Education** — training environment for production users
- **Backup** — disaster recovery site

Projects may adapt the model, for example:
- DTAPB
- DTP
- DTEP

---

## Infrastructure as Code (IaC)

Infrastructure as Code means managing and provisioning infrastructure through code instead of manual processes.

Why it matters:
- infrastructure specifications are stored in configuration files
- configurations are easier to edit and distribute
- teams can provision the same environment every time
- it helps avoid undocumented, ad-hoc configuration changes

### Ansible
Ansible is an open-source toolset that supports IaC.

It includes:
- software provisioning
- configuration management
- application deployment

---

## Advanced deployment strategies

### Blue-Green Deployment
Blue-green deployment runs two near-identical environments in production:
- **Blue** = old version
- **Green** = new version

How it works:
- traffic is gradually transferred from blue to green
- if green is stable, blue can be kept on standby or updated for the next cycle

Main advantage:
- fast rollback if needed

### Canary Release
A canary release sends changes to a small subset of users first.

Why teams use it:
- observe real user interaction
- limit the impact of failures
- perform built-in capacity testing
- gather real user feedback
- reduce cold-start issues
- support no-downtime upgrades
- allow easy rollback

### A/B Testing
A/B testing deploys two versions to different groups of users to compare which performs better.

Useful for:
- testing new features
- testing design changes before full rollout

### Feature Flags
Feature flags allow features to be turned on or off for selected users or user groups.

Useful for:
- gradual rollout
- controlled testing of new features

---

## Deployment plan template
The lecture gives a deployment plan template with fields such as:
- Sequence Number
- Activity Name
- Activity Description
- Scripted Instruction
- Start Date & Time
- Expected Duration
- Dependent Activities
- Responsible Resource

A deployment template is described as an unbound deployment plan that defines the steps of execution.

---

## Quick comparison

### Blue-Green vs Canary
**Blue-Green**
- switches traffic between two full environments
- strong rollback path
- both versions run in production

**Canary**
- exposes only a small subset of users first
- smoother rollout
- lower blast radius if something goes wrong
- useful for real-world observation before full release

### A/B Testing vs Feature Flags
**A/B Testing**
- compare two versions to measure performance or user response

**Feature Flags**
- enable or disable a feature for chosen users or groups

---

## Revision checklist
Make sure you can explain:
- definition of software deployment
- release, installation, activation, deactivation, uninstallation, update
- Local / Development / Integration / Testing / Staging / Production
- DTAP
- IaC and why it helps
- Ansible
- blue-green deployment
- canary release and its benefits
- A/B testing
- feature flags
- deployment plan template

---

## Scope note
These notes focus on **Topic 5: Deployment**.  
The uploaded PSD_6 file also contains extra material on **PERT** and **FSM**, which aligns with the uploaded Tutorial 05 files rather than the main deployment lecture.
