# Exercise 8 — When to Use Which? (Decision Guide)

## Goal

Know which customization to reach for in any situation.

---

## The Decision Flowchart

```
Is this something that should ALWAYS apply?
├─ YES → Is it specific to certain file types?
│        ├─ YES → Scoped Instruction (.instructions.md with applyTo)
│        └─ NO  → Project Instruction (copilot-instructions.md)
│
└─ NO  → Is it a specific task/workflow you trigger on demand?
         ├─ YES → Skill (SKILL.md)
         └─ NO  → Does it need a specialized persona + tools?
                  ├─ YES → Agent (*.agent.md)
                  └─ NO  → Just put it in your prompt
```

---

## Real-World Examples

| Scenario | Use | Why |
|---|---|---|
| "All Angular components should use standalone + Signals" | **Instruction** | Applies to every component, every time |
| "SCSS should follow BEM naming" | **Scoped Instruction** (`*.scss`) | Only relevant to SCSS files |
| "All code should be OWASP compliant" | **Instruction** (global) | Always-on security baseline |
| "Audit a component for accessibility" | **Skill** | On-demand action with a workflow |
| "Generate a conventional commit message" | **Skill** | Repeatable task, invoked when needed |
| "Review my code as a senior Angular architect" | **Agent** | Needs a persona + expertise + tool access |
| "Help me with Terraform infrastructure" | **Agent** | Specialized domain + tools (terminal, MCP) |
| "Tell me a joke about my code" | **Skill** | Fun on-demand action |
| "Always add a fun fact to responses" | **Instruction** | Always-on communication rule |

---

## For .NET Developers

The same concepts apply to your .NET projects:

| Customization | .NET Example |
|---|---|
| **Instruction** (global) | "Use nullable reference types. Follow SOLID principles. Use async/await for I/O." |
| **Scoped instruction** | `applyTo: '**/*.cs'` → "Use primary constructors. Prefer records for DTOs." |
| **Scoped instruction** | `applyTo: '**/*.cshtml'` → "Use Tag Helpers, not HTML Helpers." |
| **Skill** | `/generate-api-endpoint` — scaffolds a controller, service, and DTO |
| **Agent** | ".NET Architect" — reviews for clean architecture, DDD patterns, EF Core best practices |

---

## Quick Reference Card

| | Instructions | Skills | Agents |
|---|---|---|---|
| **File** | `*.instructions.md` | `SKILL.md` in a folder | `*.agent.md` |
| **Location** | `.github/instructions/` or `.github/copilot-instructions.md` | `.github/skills/<name>/` | `.github/agents/` |
| **Activated** | Automatically (passive) | On demand (`/command` or agent discovery) | Explicitly selected |
| **Scoping** | `applyTo` glob patterns | N/A (invoked explicitly) | N/A (selected explicitly) |
| **Purpose** | Coding standards, conventions | Reusable tasks, workflows | Personas, expertise, tool access |
| **Stacks** | All matching instructions apply | Can be invoked by agents | Agents read project instructions |
| **Think of it as** | Your team's rulebook | Your team's toolbox | Your team's specialist |

---

## Final File Structure

Everything we built during this workshop:

```
.github/
├── copilot-instructions.md                    ← Ex 2: global instructions
├── instructions/
│   ├── angular-frontend.instructions.md       ← Ex 3: scoped to TS/HTML
│   ├── scss-styling.instructions.md           ← Ex 3: scoped to SCSS
│   ├── security.instructions.md               ← Ex 3: scoped to everything
│   └── fun-personality.instructions.md        ← Ex 4: the proof it works
├── skills/
│   ├── tell-a-joke/
│   │   └── SKILL.md                           ← Ex 5: fun skill
│   └── accessibility-audit/
│       └── SKILL.md                           ← Ex 5: practical skill
└── agents/
    ├── angular-architect.agent.md             ← Ex 6: practical agent
    └── chandler-bing.agent.md                 ← Ex 6: fun agent
```

---

## The Key Takeaway

> **Don't repeat yourself in prompts.** If you're adding the same context to every prompt, it belongs in an instruction file. If you're running the same task repeatedly, make it a skill. If you need a specific persona or workflow for a whole session, create an agent.

---

**Previous:** [Exercise 7 — Putting It All Together](exercise-7-all-together.md)
**Back to:** [Workshop Overview](../WORKSHOP.md)
