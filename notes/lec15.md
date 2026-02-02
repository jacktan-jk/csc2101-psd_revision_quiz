# Topic 4 — Cloud Native & Microservices (Revision Notes)

## What “cloud native” means
- An approach to building and running applications that are:
  - **scalable**
  - **resilient**
  - **flexible**

## Monolithic architecture
### Characteristics
- One unit of deployment.
- All functionalities/processes tightly coupled.
- Runs as a single service.

### Common limitations
- Adding new features becomes more complex over time.
- Lock‑in to a particular technology stack.
- Low fault tolerance.
- Scaling limitations.

## Microservices architecture
### Core idea
- Break an application into smaller services (each focused on a capability) that can be deployed independently.

### Why microservices
- **Flexibility**: smaller chunks allow teams to split ownership and use different tools/methods.
- **Reliability**: decoupling reduces risk; if one service fails, impact is isolated.
- **Scalability**: scale individual services as needed; target resources where most needed.
- **Agility**: independent deployment enables faster change delivery.

## Communication patterns
### Synchronous communication
- Request–response style (e.g., REST API).
- Typical characteristics: HTTP request/response, JSON payloads, verbs like GET/POST/PUT/DELETE.

### Asynchronous communication
- Event-driven messaging (services don’t wait for immediate responses).

#### Message Queue (point-to-point)
- Exactly one delivery.
- Exactly one consumer.
- Messages are not ordered (as presented in the material).

#### Publish–Subscribe channel
- At least one delivery.
- Multiple consumers allowed.
- Ordered messages (as presented in the material).

## Containers
### What a container is
- A standardised unit for development, deployment, and distribution.
- Packages code and all dependencies, including:
  - language runtimes
  - executables / binaries
  - libraries
  - configuration files
- Abstracts apps from the environment they run in.

### Why microservices commonly use containers
- Portability across environments.
- Massive horizontal scalability.
- High availability and redundancy.

## Container orchestration
### Kubernetes (as introduced)
- An open-source orchestration system used for managing and scaling containers automatically.
- Key orchestration features highlighted:
  - self-healing
  - auto-scaling
  - rolling updates
  - self-service
  - automation of microservice management

## Professor revision-style prompt patterns
- Compare monolith vs microservices in scalability and fault tolerance.
- Explain why decoupling improves reliability.
- Identify when to use synchronous vs asynchronous communication.
- Define containers and why orchestration is needed at scale.
