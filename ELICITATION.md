# Elicitation Library

**Techniques for pushing AI models past their default average output.**

---

## Why This Exists

When you ask an AI model a question, you get the middle of the bell curve. Competent, reasonable, forgettable. That's fine for casual use. It's not fine when you're building production software where decisions compound.

Elicitation techniques are how you push the model off that comfortable center. You're not prompting harder. You're changing the structure of how the model thinks about the problem.

Use these at any point in the JFMAD workflow. During architecture review, during story writing, during adversarial consensus rounds. Anywhere you suspect the output is "good enough" instead of actually good.

---

## The Techniques

### 1. Hindsight is 20/20

Tell the model to imagine the project launched 6 months ago. It's sitting in a retrospective. What "if only" statements come up?

**When to use:** After drafting requirements, architecture, or scope decisions.

**How:** "Imagine this shipped 6 months ago. What 'if only we had...' and 'if only we hadn't...' statements would come up in the retrospective?"

**Why it works:** Forces the model to evaluate decisions from the perspective of consequences, not intentions. Cuts scope better than any prioritization framework.

### 2. Red Team / Blue Team

Split the model into two roles. Blue team defends the current approach. Red team tries to break it. Run 2-3 rounds.

**When to use:** Architecture decisions, security review, API design.

**How:** "Red team this architecture. Find every way it could fail, be exploited, or cause maintenance headaches. Then defend it as blue team. Then red team the defense."

**Why it works:** Adversarial consensus is a JFMAD core principle. This formalizes it within a single model when you need quick validation.

### 3. Stakeholder Roundtable

Have the model simulate perspectives from different roles looking at the same decision.

**When to use:** When a decision affects multiple concerns (performance, UX, cost, timeline).

**How:** "Evaluate this decision as: (1) the user who has to live with it, (2) the developer who has to maintain it, (3) the PM who has to explain it, (4) the CTO who has to scale it."

**Why it works:** Single-perspective analysis misses tradeoffs. This surfaces conflicts before they become production bugs.

### 4. Assumption Audit

Have the model list every assumption baked into its recommendation, then challenge each one.

**When to use:** After any significant recommendation or architecture proposal.

**How:** "List every assumption in this recommendation. For each one, what happens if it's wrong?"

**Why it works:** AI models present assumptions as facts. This technique forces them to the surface where you can evaluate them.

### 5. Five Whys (Applied)

Take any design decision and ask "why" five times in sequence.

**When to use:** When something feels right but you can't articulate why, or when something feels off.

**How:** "Why did you choose this database? [answer] Why does that matter for this use case? [answer] Why is that more important than [alternative]? ..."

**Why it works:** Surfaces the actual reasoning chain. By the third why, you'll know if the decision is grounded or cargo-culted.

### 6. Constraint Inversion

Remove the biggest constraint and see what changes. Then add a constraint that doesn't exist and see what changes.

**When to use:** When you feel boxed in by requirements, or when the solution feels too obvious.

**How:** "What would this architecture look like with unlimited budget? Now what would it look like if it had to run on a single $5/month server?"

**Why it works:** Reveals which constraints are actually shaping the design vs. which are just assumed.

### 7. Pre-Mortem

Before building, imagine the project failed completely. Why?

**When to use:** Before committing to an approach. Before sprint planning.

**How:** "This project failed. Users hated it, the codebase is unmaintainable, and we're starting over. What went wrong?"

**Why it works:** Easier to imagine specific failure modes than to imagine all possible futures. The failures you imagine are the risks you need to mitigate.

### 8. Explain It To A Junior

Have the model explain its recommendation as if to someone with no context.

**When to use:** When architecture or code feels overcomplicated.

**How:** "Explain this architecture to a junior developer who's never seen the project. If you can't do it simply, simplify the architecture."

**Why it works:** Complexity that can't be explained simply is complexity that can't be maintained. This is a forcing function for clarity.

---

## How Many to Use

Don't use all of them on everything. That's a recipe for analysis paralysis.

**For routine decisions:** Pick one. Assumption Audit is usually the highest ROI.

**For major architecture choices:** Pick two or three. Red Team + Hindsight + Stakeholder Roundtable is a strong combo.

**For scope decisions:** Hindsight is 20/20 alone will save you more time than anything else in this document.

---

## Making It Adversarial

In JFMAD, these techniques get more powerful when applied across models. Run the Assumption Audit with Claude, then hand the assumptions to ChatGPT and ask it to challenge them. Have Gemini red-team the architecture that Claude designed.

Single-model elicitation is useful. Cross-model elicitation is where JFMAD's multi-model approach really earns its keep.

---

*These techniques draw from prompt engineering research, competitive prompting competitions, and practical experience. Some overlap with elicitation methods in the [BMAD Method](https://github.com/bmad-code-org/BMAD-METHOD).*
