# AI Engineering Playbook

A practical, opinionated guide to building and operating AI systems in production.

This is not a list of tools or prompts.  
This is about how AI systems actually work in real-world engineering.

> AI engineering is less about writing code, and more about designing systems that work despite uncertainty.

---

## What This Covers

Instead of treating LLMs as simple code generators, this playbook focuses on how to design systems around them:

- Clear engineering guidelines
- Reusable skills
- Composable agents

---

## What This Is

AI engineering is not traditional software engineering.

It is:
- Data + prompts instead of fixed logic
- Probabilistic instead of deterministic
- Evaluation-driven instead of test-driven

This playbook focuses on:
- Building reliable AI systems
- Managing uncertainty and failures
- Designing workflows that scale

---

## What This Is Not

- ❌ A prompt collection  
- ❌ A list of AI tools  
- ❌ A theoretical machine learning guide

---

## Core Principles

1. **Evaluation > Prompting**  
   If you can’t measure outputs, you can’t improve them.

2. **Start Simple**  
   Avoid agents and complex pipelines unless absolutely necessary.

3. **Data is the real product**  
   Prompts change frequently, but data compounds over time.

4. **Design for failure**  
   AI systems are inherently unreliable — build with fallback and safeguards.

5. **Iteration > Architecture**  
   Most improvements come from faster iteration, not more complex systems.

---

## Architecture

This system is built in three layers:

### 1. Core (Behavior)
- `ENGINEERING_GUIDELINES.md`  
  Defines how problems are approached and solved.

### 2. Skills (Capabilities)
Reusable, domain-agnostic capabilities:

- `bug-fixing.md` → Structured debugging approach  
- `api-integration.md` → Reliable API handling  
- `ui-building.md` → Generic UI patterns  
- `flutter-ui.md` → Flutter-specific UI and responsive design  
- `testing.md` → Structured validation and test scenarios
- `state-management.md` → Decision system for choosing appropriate state management    

### 3. Agents (Execution)

- `feature-builder-agent.md` → Generic feature workflow  
- `flutter-feature-agent.md` → Flutter-specific feature workflow  

---

## Philosophy

- Think before coding  
- Prefer simple solutions  
- Make minimal, focused changes  
- Validate behavior, not just code  
- Avoid overengineering    

---

## Why This Exists

LLMs are powerful, but without structure they often:
- Overcomplicate solutions  
- Make unnecessary changes  
- Assume instead of verifying  

This playbook provides a disciplined approach to make LLMs behave more like production-ready engineers.

---

## Current Status

- Version: v1.2  
- Added state management decision guide  
- Introduced codebase-aware agent workflow  
- Improved decision-making for new and existing projects  

---

## Roadmap

- Add more domain-specific skills  
- Improve agent workflows  
- Introduce real-world examples  
- Expand testing and validation patterns  

---

## Goal

Create a system where:
- Guidelines define behavior  
- Skills define capabilities  
- Agents execute real-world tasks  

---

## Inspiration

This playbook is influenced by:
- Andrej Karpathy’s perspective on AI engineering as a new software paradigm
- Open-source AI engineering playbooks and community best practices
- Real-world experience building and operating production AI systems

Rather than repeating existing ideas, this repository focuses on making them practical, opinionated, and directly usable in day-to-day engineering workflows.
