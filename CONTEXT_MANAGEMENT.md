# Context Management

**How to keep your AI team sharp when projects get complex.**

---

## The Problem

Every AI model has a context window. The more you stuff into it, the worse it performs. Not dramatically. Subtly. It starts missing details. It contradicts earlier decisions. It "forgets" constraints you set 40 messages ago.

In a multi-model workflow like JFMAD, this compounds. Each model is making decisions that affect all the others. If the architect's context is polluted with PM conversations, or the developer is loading the full constitution when it only needs the tech stack, you're wasting capacity and inviting drift.

Context management is how you keep every model working with exactly what it needs and nothing more.

---

## Three Rules

### 1. Fresh Context Per Role Switch

Every time you switch from one model/role to another, start a clean session. Don't carry the architect's conversation into the PM's review. Don't let the developer inherit the QA discussion.

**Why:** Each role needs to evaluate the work product independently. Carrying context forward creates confirmation bias. The developer who just wrote the code shouldn't be reviewing it in the same session. The PM who debated the requirements shouldn't be the one validating them.

**How:** Save the output (document, decision, story) to a file. Start a new session. Load only what the next role needs.

### 2. Document Sharding

Large documents kill context efficiency. A 50-page architecture doc means every agent loads 50 pages whether it needs 2 paragraphs or all 50.

Split large documents into focused pieces:

**Architecture splits into:**
- `architecture/tech-stack.md` - Languages, frameworks, versions, and why
- `architecture/source-tree.md` - Project structure and file organization
- `architecture/coding-standards.md` - Style, documentation, naming conventions
- `architecture/data-models.md` - Interfaces, schemas, relationships
- `architecture/api-contracts.md` - Endpoints, request/response shapes

**Requirements split into:**
- `requirements/epics.md` - High-level feature groups
- `requirements/stories/` - Individual stories, one file each
- `requirements/nonfunctional.md` - Performance, security, accessibility

**Constitution stays whole.** It's your source of truth. Every role needs access to it. But it should be concise enough to not bloat context.

### 3. Load Configs Per Role

Each role in your team should have a defined list of documents it always loads, and nothing else.

**Architect always loads:**
- Constitution
- Tech stack
- Data models
- Source tree

**PM always loads:**
- Constitution
- Epics overview
- Current sprint plan

**Developer always loads:**
- Current story file (contains everything it needs)
- Tech stack
- Coding standards
- Source tree

**QA always loads:**
- Current story file
- Coding standards
- The actual source code being reviewed

The developer doesn't need the PM's epic breakdown. The PM doesn't need the coding standards. Keep it surgical.

---

## Story-Level Context Engineering

This is the most impactful practice in this document.

When preparing a story for the developer, don't just write "implement user authentication." Pull in the specific sections from architecture, the relevant data models, the coding standards that apply, and the acceptance criteria. Bundle it all into the story file itself.

The developer should be able to open one file and have everything it needs. No searching. No loading extra documents. No context wasted on irrelevant architecture sections.

**A good story file contains:**
- What to build (acceptance criteria)
- How to build it (relevant architecture excerpts)
- Where to put it (source tree reference)
- What standards to follow (relevant coding standards)
- What to call things (relevant data model excerpts)
- What was done before this (notes from previous story, if any)

**A bad story file says:** "Implement story 3.2 per the architecture doc."

The difference between these two approaches is the difference between a developer that stays on the rails and one that invents its own architecture mid-build.

---

## When Context Gets Too Large

Signs your context is bloated:
- The model starts contradicting earlier decisions
- It "forgets" constraints you set earlier in the conversation
- Responses get vague or generic
- It starts suggesting libraries or patterns not in your tech stack

**What to do:**
1. Save your current output to a file
2. Start a fresh session
3. Load only the documents relevant to your next task
4. Reference the saved output if needed

Don't rely on compaction (automatic context trimming). It randomly drops things that might be critical. Manual context management is slower but predictable.

---

## The Payoff

Clean context means:
- Models follow your tech stack instead of inventing their own
- Decisions stay consistent across sessions
- Stories get implemented as specified, not as improvised
- QA catches real issues instead of re-litigating architecture

This isn't overhead. This is how you prevent the rework cycles that make AI-assisted development feel unreliable.

---

*Context engineering principles informed by practical multi-model development experience and techniques documented in the [BMAD Method](https://github.com/bmad-code-org/BMAD-METHOD).*
