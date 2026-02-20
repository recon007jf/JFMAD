# JFMAD — Joseph Fagan's Method for Agile AI-Driven Development

**A development methodology for building production software using multiple specialized AI models as an adversarial team, governed by living constitutional documents.**

---

## The One-Sentence Version

> *"I don't code. I don't prompt. I architect decisions, assign them to the right intelligence, and make sure every output earns the trust of the person whose name is on it."*

---

## What Is JFMAD?

JFMAD is a methodology for coordinating multiple AI models as a structured development team — with real roles, real accountability, and real governance — to build production software.

It was developed organically by [Joseph Fagan](https://github.com/josephfagan) during the construction of an AI-powered sales intelligence platform, from November 2025 to present. The methodology wasn't planned. It emerged from the practical demands of building a production system for a real client whose reputation was on the line.

In February 2026, Joseph discovered that a similar framework called [BMAD](https://github.com/bmad-code-org/BMAD-METHOD) (Breakthrough Method of Agile AI-Driven Development) had been published independently in April 2025. JFMAD was not derived from BMAD — it converged on many of the same structural conclusions through practice rather than theory.

This is convergent evolution. BMAD was designed as a theory-first framework: "here's how AI development teams should be structured." JFMAD arrived at the same conclusions empirically: "this is what I had to do to stop things from breaking."

---

## Why Does This Exist?

Most people using AI for development are doing one of two things:

1. **Vibe coding** — ad hoc prompting, hoping for good output, losing context constantly
2. **Single-model workflows** — using one AI as a copilot, re-explaining everything every session

Both break down the moment you're building something real — something with users, reputation stakes, and production constraints.

JFMAD solves this by treating AI models the way you'd treat a development team: specialized roles, structured handoffs, adversarial review, and living documentation as the institutional memory that no single session can hold.

---

## The Six Principles

### 1. Model-Native Role Assignment

Don't role-play — cast. Each AI model is chosen for a role because it is genuinely better at that function.

- **Claude** thinks in systems → Systems Architect
- **ChatGPT** enforces process → Product Manager
- **Gemini** catches technical risk → Technical Lead
- **Your developer** (human or AI) ships code → Lead Developer
- **You** set direction and make final calls → Visionary / Project Owner

The role fits the tool, not the other way around. This isn't one model pretending to be five people. It's five different intelligences doing what they're each best at.

### 2. Adversarial Consensus

Every decision gets pressure-tested at each level before reaching implementation.

Architecture gets challenged by process constraints. Sequencing gets validated against technical feasibility. Nothing reaches code without surviving the gauntlet.

**The friction is the feature.** This isn't dysfunction — it's how you prevent the rework cycles that kill AI-assisted projects.

Chain of command: **Visionary → Architect → PM → Tech Lead → Developer**

### 3. Constitutional Governance

The system is governed not by requirements documents but by a **living constitution** that defines:

- What the product does and why
- How the AI behaves on behalf of real people
- What design principles are non-negotiable
- What decisions are locked and why

Sprint specs, architecture decisions, and behavioral calibration all trace back to the constitution. It's not a PRD — it's a behavioral contract. See [templates/CONSTITUTION_TEMPLATE.md](templates/CONSTITUTION_TEMPLATE.md).

### 4. Client as Co-Creator

The end user is not a passive stakeholder submitting feature requests. Their feedback is treated as **constitutional amendments** — direct inputs that reshape how the system reasons.

Their exact phrasing matters. Their tone preferences become system constraints. Their discomfort with a draft isn't a bug report — it's a calibration signal.

### 5. Institutional Memory via Documentation

No single AI session holds the full picture. Your documentation workspace (Notion, Obsidian, whatever) serves as the team's shared brain:

- **Constitution** — what the product is and how it behaves
- **Roadmap** — what's built, what's next, what's locked
- **Project Principals** — who everyone is, their roles, relationships, correct names
- **Sprint Plans** — what's being built right now and why
- **Methodology** — how the team operates (this document)

You point to docs instead of re-explaining context. **If it's not documented, it didn't happen. If it's documented, it's the source of truth.**

See [templates/](templates/) for starter structures.

### 6. Plain Text Directives

All instructions to the development team are delivered as plain text in chat, never as documents or files.

This prevents misinterpretation and keeps the implementation layer focused on exactly what was specified. A developer (human or AI) should be able to read the directive and know precisely what to build without opening any attachments.

---

## JFMAD vs BMAD

| Concept | BMAD | JFMAD |
|---|---|---|
| **Role assignment** | Roles via system prompts to a single LLM | Roles assigned to different AI models based on cognitive strengths |
| **Orchestration** | Single orchestrator agent manages sub-agents | Human visionary orchestrates with explicit chain of command |
| **Governance** | PRDs and architecture docs | Living constitutional documents governing AI behavior |
| **Review process** | Role-based review stages | Adversarial consensus — every decision pressure-tested at each level |
| **Client role** | Stakeholder providing requirements | Co-creator whose feedback becomes constitutional amendments |
| **Memory** | Semantic memory within agent framework | Institutional memory via documentation workspace |
| **Handoffs** | Automated through agent pipelines | Plain text directives — deliberate, no documents |
| **Origin** | Theory-first framework (April 2025) | Practice-first discovery (November 2025) |

BMAD and JFMAD are complementary, not competing. BMAD provides excellent tooling for agent prompt management. JFMAD provides the governance philosophy and multi-model team structure that makes production systems trustworthy.

---

## What JFMAD Built

Using this methodology, a single person (Joseph Fagan) built in ~3 months what would typically require 9-12 months and $400-600K with a traditional development team:

- Proprietary data pipeline combining DOL filings, BenefitFlow, and PDL enrichment
- Deterministic scoring engine with narrative intelligence
- AI drafter calibrated to a specific person's voice and market context
- Morning plan workflow across 8 Western Region states
- Live production application with safety gates
- 97+ contract tests with zero regressions
- Constitutional design framework governing AI behavior

The product is in alpha with a real client making real outreach decisions.

---

## Getting Started

1. **Read the [Six Principles](#the-six-principles)** above
2. **Copy the templates** from [templates/](templates/) into your project
3. **Assign your models** — decide which AI handles which role based on what it's actually good at
4. **Write your constitution first** — before any code, define what the product is, who it serves, and what's non-negotiable
5. **Establish your chain of command** — who reviews what, in what order
6. **Document everything in one workspace** — Notion, Obsidian, whatever. This is your institutional memory.

---

## Templates

- [CONSTITUTION_TEMPLATE.md](templates/CONSTITUTION_TEMPLATE.md) — Starter structure for your product's governing document
- [ROADMAP_TEMPLATE.md](templates/ROADMAP_TEMPLATE.md) — Project roadmap with phase gates and sprint tracking
- [PRINCIPALS_TEMPLATE.md](templates/PRINCIPALS_TEMPLATE.md) — Source of truth for every person involved in the project

---

## Philosophy

JFMAD exists because AI-assisted development has a trust problem. The tools are powerful but ungoverned. Output is fast but unreliable. Context is rich but ephemeral.

The solution isn't better prompts. It's better structure. The same structure that makes human teams effective — specialized roles, adversarial review, institutional memory, clear authority — makes AI teams effective too.

The only difference is that you're the one holding it all together.

---

## License

MIT License. Use it, adapt it, make it yours. Attribution appreciated.

---

## Author

**Joseph Fagan** — Creator of JFMAD

*JFMAD formalized February 2026. Based on organic practice established November 2025.*
