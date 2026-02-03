# Software Engineering Confidence Roadmap (Hands-on & Mindset Driven)

This readme outlines a guided, mentor-driven roadmap to become a strong, confident, and well-rounded software engineer. It emphasizes understanding the “why” before the “how,” incremental projects, real-world practices, documentation, and mindset growth. The focus is on confidence through preparation and repetition, not speed.

---

## 🎯 Core Goal

- Build confidence through a steady, evolving project that grows in complexity
- Ground learning in strong fundamentals (not shortcuts)
- Practice real-world engineering processes (version control, architecture, testing, CI, deployment, IaC)
- Document, reflect, and iterate (documentation as a learning instrument and portfolio)
- Embrace trade-offs and diverse approaches; there is no single “right” way

---

## 🧠 Guiding Philosophy

- Confidence comes from preparation and repetition
- Start small, grow gradually; keep scope manageable
- Tie every concept to practical, real-world use
- Documentation is part of learning and portfolio-building
- Explore trade-offs; celebrate multiple valid approaches

---

## 📂 Organization Rules

- Use Notion as the main learning journal

### 📁 Notion Structure

- Create a main Notion page with the name of your project (represents the single evolving system, e.g., “User Manager API”)
- Create one subpage for each milestone to document the evolution at that stage

### 📄 Milestone Subpage Requirements

Each milestone subpage must include:
- What was built
- How it was built
- Questions and unknowns
- Errors and how they were solved
- Personal reflections
- What was learned
- What should not be repeated

### 🧭 Documentation Guidelines

- Use Table of Contents inside each milestone page
- Include diagrams and mental models (Whimsical, draw.io, Mermaid, etc.)
- Aim for clear narrative: decisions, rationale, and evolution

---

## 🧩 Issue Categories

- **[TECH]** — Technical implementation
- **[ME]** Mindset Evolution — Reflection and reasoning
- **[HO]** Hands-On — Small practical challenges / POCs

### Issue Note

Each milestone will include sample issues in these categories to practice reporting, reflecting, and learning.

---

## Branch Naming Convention

- Use the format: `milestone-{milestone_number}-{short_description}-username-feature_short_description`
  - Example: `milestone-1-start-up-johndoe-add-swagger`

---

## 🛣️ Roadmap Sequence (Must Follow This Order)

The milestones are designed to be tackled in the order listed below. Each milestone builds on the previous ones, reinforcing fundamentals and expanding scope with deliberate practice.

---

## Milestone 0 — Git and GitHub Fundamentals

**Purpose:** Foundations for collaboration, history tracking, and professional workflows.

### Goals
- Grasp what Git is and why it exists
- Understand collaboration before Git (manual versioning, FTP, shared folders)
- Use GitHub effectively for collaboration

### Tasks
- Create a project on GitHub
- Add mentor as a collaborator
- Commit and push code regularly
- Block commits to main without PRs; PRs must be reviewed/approved before merging
- Use feature and fix branches

### Concepts to Understand
- What is Git? What problems does VCS solve?
- Commits: purpose, size, and messaging
- Pre-Git era: FTP/shared folders/backups
- Branching and merging basics

### [ME] Issues (Reflection)
- Why version control is non-negotiable
- Why commit history is documentation and learning

### [HO] Hands-On Challenges
- Create a small project and manage it with Git
- Practice branching, merging, and PR reviews

---

## Milestone 0.1 — Programming Languages & Execution Model Fundamentals

**Goal:** Understand how languages are executed, what happens between writing code and running it, and the role of the runtime.

### Topics to Explore
- Interpreted vs compiled languages
- Hybrid execution models
- How the .NET compilation pipeline works (as a reference case)
- Compile-time vs runtime
- Just-In-Time (JIT) compilation and its trade-offs

### Concepts to Understand
- Source code vs machine code
- Intermediate Language (IL)
- Assemblies (.dll, .exe)
- Common Language Runtime (CLR)
- JIT vs AOT and trade-offs

### [ME] Issues (Reflection)
- Why understanding execution models makes you a better engineer
- What parts of language execution still feel “magical”
- How this knowledge changes debugging and performance reasoning

### [HO] Challenges
- Draw a diagram of the .NET execution flow
- Explain JIT to someone with no backend background

---

## Milestone 1 — Start Up

- Create a simple .NET API
- Single layer only
- No tests
- No database (in-memory list)
- Focus on project startup and configuration
- Add unanswered questions at the end
  - What is a Web API project?
  - What are the types of .NET projects and why they’re used? (Console app, class library, Web API)
- Add Swagger to the project (and Swagger UI)

### Learning Goals
- Understand project structure and startup configuration
- Explore basic API design concepts and routing
- Learn how to expose API metadata (Swagger)

### [HO] Hands-On Challenges
- Create a minimal Web API with CRUD using in-memory storage
- Add Swagger and verify UI

### [ME] Reflection/Questions
- Why is a minimal API a good starting point?
- Trade-offs between minimalism and future extensibility

---

## Milestone 1.1 — REST API Best Practices

### Goals
- Proper HTTP verbs and routes
- Consistent API responses
- Use `ActionResult` / `ActionResult<T>`
- Correct HTTP status codes
- Swagger configuration

### [HO] Hands-On Challenges
- Refine endpoints to follow REST conventions
- Implement consistent error and success responses

### [ME] Reflection
- How do HTTP semantics influence API design?
- When should you deviate from REST conventions (e.g., RPC-ish endpoints)?

---

## Milestone 1.2 — Architecture of the API

### Goal
Understand why software architecture exists and how structuring code into layers improves maintainability and evolution.

### Challenge
Refactor the User Manager API to introduce clear architectural boundaries.

### What You Will Do
- Add a Domain layer
- Separate responsibilities by layer
- Move business logic out of controllers
- Define clear dependencies between layers
- Inject services via dependency injection

### Concepts to Understand
- What is software architecture?
- Layering, boundaries, and dependency direction
- Benefits and trade-offs
- Dependency injection and DI types

### [ME] Issues
- Why “just working code” is not enough
- How bad architecture slows teams down
- When simplicity beats abstraction

### [HO] Challenges
- Diagram the layered architecture
- Explain DI concepts to someone non-technical

---

## Milestone 1.3 — Validation

### Goal
Understand why validation exists, where it should live, and what responsibilities belong to the application.

### Challenge
Reflect on current use of FluentValidation and explore alternatives.

### Reflection Questions ([ME])
- Why is FluentValidation a good choice here?
- Why is application-layer validation appropriate?
- Pros and cons of this approach?

### Validation Strategies to Explore
- Data annotations
- Domain-level validation
- Database constraints
- Frontend validation
- External validation services
- Throwing exceptions

### Key Insight
There is no single correct validation strategy. Trade-offs matter.

---

## Milestone 2 — Automated Tests

- Learn the testing lifecycle from scratch
- Introduce Application layer testing
- NUnit + FluentAssertions
- Arrange / Act / Assert
- Tests describe business rules, not implementation

### [ME] Issues
- Why unit tests matter
- Test Pyramid vs Test Trophy vs Test Honeycomb
- TDD pros and cons
- Test coverage myths
- Other .NET testing options

---

## Milestone 2.1 — HTTP and DNS

- Deep understanding of HTTP
- DNS resolution flow
- Statelessness
- Performance implications
- What happens when an API is called

### [ME] Issues
- HTTP status codes nuances
- DNS reliability and networking vs application bugs

---

## Milestone 3 — Continuous Integration

- CI concepts and team culture
- GitHub Actions pipelines
- Build → Tests
- Block merge on failure

### [ME] Issues
- CI as culture, not just tooling
- Responsibility when pipelines fail
- CI vs CD

---

## Milestone 4 — Docker

- Containers vs VMs
- Containers as OS processes vs VMs
- Docker fundamentals
- Dockerfiles
- Docker Compose

### [ME] Issues
- Docker’s role in container ecosystem
- What Docker solves (and doesn’t)
- Alternatives to Docker

---

## [HO] Hands-On — Dockerflix

- Full-stack app (Angular frontend, Node backend)
- Dockerfile for frontend and backend
- Docker Compose to run both
- Frontend consumes backend API
- Push images to Docker Hub
- Validate everything running via Docker

---

## Milestone 5 — Local Database

- Introduce a real database
- Run database locally using Docker Compose
- Configure application connection
- Persist and retrieve data
- Reproduce the full system with a single command

---

## Milestone 6 — Migrations

- Understand schema evolution
- Introduce database migrations
- Apply migrations locally
- Version database changes
- Understand rollback strategies and risks

---

## Milestone 7 — Publishing the API to a Public URL

- Deploy the API publicly
- Configure environment-specific settings
- Handle secrets securely
- Validate external access
- Understand public vs private services

---

## Milestone 8 — Continuous Delivery (CD)

- Extend CI into CD
- Automate deployments
- Ensure deploys happen only after validation
- Understand release strategies and risks
- Keep the system always deployable

---

## Milestone 9 — Infrastructure as Code (IaC)

- Manage infrastructure using code
- Understand infrastructure drift
- Use declarative tools (e.g., Terraform)
- Version and review infrastructure changes
- Integrate IaC with CI/CD pipelines

---

## ✅ Expected Output

Generate:
- Milestones with clear descriptions
- Issues per milestone
- [ME] reflection questions
- [HO] hands-on challenges
- Clear learning goals per step
- A motivating, mentor-style tone

Avoid:
- Over-engineering early steps
- Skipping fundamentals
- Tool-first learning without understanding

---

## ❤️ Final Note

This roadmap is a guided journey, not a mere checklist. The aim is confidence, clarity, and sound engineering judgment—not just speed.

---

## Example Issue Templates (Ready-to-Use in Notion)

> These are ready-to-adapt templates you can paste into Notion as a starting point for each milestone.

### Example of TECH Issue

Details
- The main goal of this first step is to be familiar with startup project concepts. It takes time and effort to get things working; expect trials and errors.

Goal
- Create a simple API to manage users (CRUD) with in-memory data for the initial milestone.

Challenge
- Build a minimal API to manage users:
  - Add a new user
  - Update an existing user
  - Delete a user
- Keep this step simple; we will extend later.

### Example of TECH Issue (CI)

Details
- Introduce Continuous Integration to your project with a GitHub Actions pipeline.

Requirements
- Create a CI pipeline for the project using GitHub Actions
- Run on every pull request to main
- Steps: Build, Run automated tests
- Build must precede tests
- PRs should be blocked until pipeline passes

Expected Behavior
- If build fails, tests do not run
- If any test fails, PR cannot be merged
- A successful pipeline means the project builds and tests pass

Key Principles
- CI is a quality gate, not just automation
- Fail fast and visible
- Pipeline should be simple and understandable

### Example of ME Issue Template

Details
- Reflection exercise to explore the purpose and value of unit testing

Questions to Answer
1. Why should we do unit tests?
2. What is the Test Pyramid?
3. What is TDD?
4. Is >80% test coverage necessary?
5. Learn about alternative models: Test Trophy, Test Honeycomb

What to Produce
- Structured answers with headings, examples, diagrams, pros/cons
- Personal conclusions and reasoning

Why This Is Valuable
- Understands testing strategy and its impact on quality

### Example of HO Challenge Template: Dockerflix

Details
- Build a simple full-stack application run entirely with Docker and Docker Compose

Repository Structure
- /docker/dockerflix
  - /frontend
  - /backend

Frontend
- Location: /docker/dockerflix/frontend
- Tech: Angular
- Pages: Home (/), Series (/series) (fetch from backend)
- Ports: Frontend port 3000
- Backend must provide series data (5 items) via /series, status at /status
- Docker-related: Dockerfile for frontend, Dockerfile for backend, docker-compose.yml

Backend
- Location: /docker/dockerflix/backend
- Tech: Node.js
- Endpoints: GET /status (text), GET /series (JSON array of 5 strings)
- Ports: 4050

Docker Compose
- Connect frontend and backend via service names
- Expose frontend for browser access
- Validate through docker compose up

Validation
- Open frontend in browser, navigate to /series, ensure 5-series list renders

Learning Goals
- Understand multi-container apps and inter-service communication
- Practice Dockerfile creation for frontend/backend
- Use Docker Compose for local environments

---

If you’d like, I can tailor this readme to a specific stack (e.g., Node/Express or .NET Core + React) or adapt the milestones to your preferred pace. I can also generate a starter Notion export (text blocks you can paste into Notion) or provide ready-to-use templates for each milestone page.