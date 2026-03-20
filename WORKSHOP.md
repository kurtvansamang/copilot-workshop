# GitHub Copilot Customization Workshop

## Instructions, Skills & Agents — From Repetitive Prompts to Reusable Context

---

## Prerequisites

- VS Code with GitHub Copilot & Copilot Chat extensions
- Node.js 18+
- This repository cloned locally
- Basic familiarity with GitHub Copilot (covered in the previous session)

**Install the todo app dependencies before we start:**

```bash
cd angular-todo-list
npm install
```

---

## What This Workshop Covers

You already know how to prompt GitHub Copilot. But as you work with it more, you notice a pattern: you keep adding the same context to every prompt — _"follow WCAG guidelines"_, _"use OWASP best practices"_, _"use Angular Signals"_, _"write SCSS with BEM naming"_...

In this workshop, you'll learn how to **stop repeating yourself** by using three customization primitives:

| Primitive | File | Applies | Invoked |
|---|---|---|---|
| **Instructions** | `*.instructions.md` | Automatically to matching files | Passively — always active |
| **Skills** | `SKILL.md` in a folder | On demand | Explicitly via `/command` or by agents |
| **Agents** | `*.agent.md` | When selected | Explicitly by picking the agent |

**Main takeaway:** It's not just about _what_ these are, but **when to use which**.

> **Reference:** The [Awesome Copilot Learning Hub](https://awesome-copilot.github.com/learning-hub/) covers all fundamentals in depth. Bookmark it — it's your go-to reference after this workshop.

---

## Exercises

| # | Exercise | Concept |
|---|---|---|
| 0 | [Explore the App](exercises/exercise-0-explore-the-app.md) | Get familiar with the codebase |
| 1 | [The Verbose Prompt](exercises/exercise-1-verbose-prompt.md) | See the problem: repeating context |
| 2 | [Project-Level Instructions](exercises/exercise-2-project-instructions.md) | `copilot-instructions.md` — always-on global context |
| 3 | [Scoped Instructions](exercises/exercise-3-scoped-instructions.md) | `*.instructions.md` with `applyTo` — targeted guidance |
| 4 | [Fun Instructions](exercises/exercise-4-fun-instructions.md) | See the effect — make it unmissable |
| 5 | [Skills](exercises/exercise-5-skills.md) | `SKILL.md` — reusable on-demand tasks |
| 6 | [Agents](exercises/exercise-6-agents.md) | `*.agent.md` — personas with character |
| 7 | [Putting It All Together](exercises/exercise-7-all-together.md) | Combine all three |
| 8 | [When to Use Which](exercises/exercise-8-decision-guide.md) | Decision guide |

---

## How It Works

We start with a real problem — a big, verbose prompt that includes all the context every time. Then, exercise by exercise, we extract that context into the right customization layer:

1. **Exercise 0–1**: Feel the pain of repeating yourself
2. **Exercise 2–4**: Extract rules into **instructions** (always-on, automatic)
3. **Exercise 5**: Package reusable tasks into **skills** (on-demand)
4. **Exercise 6**: Build specialized **agents** (personas with expertise — including a sitcom character!)
5. **Exercise 7–8**: See them stack, and learn when to use which

All files are created inside `.github/` at the workspace root — the project starts clean, and we build up the customizations exercise by exercise.

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

## Further Reading

- **[Awesome Copilot Learning Hub](https://awesome-copilot.github.com/learning-hub/)** — The central resource for all Copilot customization topics
  - [What are Agents, Skills, and Instructions](https://awesome-copilot.github.com/learning-hub/what-are-agents-skills-instructions/)
  - [Defining Custom Instructions](https://awesome-copilot.github.com/learning-hub/defining-custom-instructions/)
  - [Creating Effective Skills](https://awesome-copilot.github.com/learning-hub/creating-effective-skills/)
  - [Building Custom Agents](https://awesome-copilot.github.com/learning-hub/building-custom-agents/)
  - [Copilot Configuration Basics](https://awesome-copilot.github.com/learning-hub/copilot-configuration-basics/)
  - [Before/After Customization Examples](https://awesome-copilot.github.com/learning-hub/before-after-customization-examples/)
- **[Awesome Copilot Directories](https://awesome-copilot.github.com/)** — Browse community-contributed [instructions](https://awesome-copilot.github.com/instructions/), [skills](https://awesome-copilot.github.com/skills/), and [agents](https://awesome-copilot.github.com/agents/)
- **[Agent Skills Specification](https://agentskills.io/home)** — The open spec that makes skills portable across coding agent systems
