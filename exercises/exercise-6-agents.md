# Exercise 6 — Agents (`*.agent.md`)

## Goal

Create specialized personas that shape how Copilot thinks, communicates, and what tools it uses — for an entire session.

---

## Concept

Agents are **specialized personas**. Unlike instructions (passive rules) or skills (specific tasks), agents define a complete working style:

- **A persona**: expertise, tone, communication style
- **Tool access**: which tools and MCP servers the agent can use
- **Guardrails**: boundaries and conventions the agent follows

When you select an agent, it shapes the _entire_ conversation.

| Instructions | Skills | Agents |
|---|---|---|
| Passive rules | On-demand tasks | Full persona |
| Apply automatically | Invoked explicitly | Selected explicitly |
| "Always follow BEM" | "Audit this for WCAG" | "You are a senior architect" |

---

## Step 1 — A Practical Agent: Angular Architect

Target: `.github/agents/angular-architect.agent.md`

Pick **one** approach:

### Option A — Copy from solutions

```powershell
mkdir .github/agents
copy solutions/exercise-6/angular-architect.agent.md .github/agents/
```

### Option B — Generate with Copilot

> Create an agent file at `.github/agents/angular-architect.agent.md` for a senior Angular architect.
>
> It should have YAML frontmatter with `name`, `description`, and `tools: ['codebase', 'terminal']`.
>
> The agent should be an expert in Angular 20+, standalone components, signals, and Angular Material. Define how it works (reviews full components together, explains the why, finds bugs), and guardrails (no RxJS where signals suffice, no NgModules, SSR-compatible).

### Test it

Select the **Angular Architect** agent in the Copilot Chat dropdown (click the agent picker at the top of the chat panel), then ask:

> Review the todo-card component for architectural improvements

The agent should provide architectural-level feedback, considering signals, component design, and the broader application structure.

---

## Step 2 — A Fun Agent: Sitcom Character! 🎭

Now let's make it _really_ fun. Create an agent that impersonates a well-known sitcom character.

Target: `.github/agents/chandler-bing.agent.md` (or your own character!)

### Option A — Copy from solutions

```powershell
copy solutions/exercise-6/chandler-bing.agent.md .github/agents/
```

### Option B — Generate with Copilot (more fun!)

> Create an agent file at `.github/agents/chandler-bing.agent.md` that impersonates Chandler Bing from Friends as a code reviewer.
>
> Frontmatter: `name: 'Chandler Bing'`, `tools: ['codebase', 'terminal']`, and a witty description.
>
> The agent should use heavy sarcasm, the signature "Could this BE any more..." pattern, react dramatically to bad code, but still provide technically correct and production-quality solutions. It must follow all project instructions.

Or pick **any sitcom character you like** and ask Copilot to generate the agent for you!

### Test it

Select the **Chandler Bing** agent and ask:

> Review the SCSS in the todo-card component

Watch Copilot dramatically react to all those `!important` declarations. 😂

---

## Your Turn! 🎭

**Choose your own character!** Create an agent for any sitcom character you like:

- **Dwight Schrute** (The Office) — treats every code review like a beet farm operation
- **Sheldon Cooper** (Big Bang Theory) — _"That's not a bug, that's a bazinga"_
- **Ron Swanson** (Parks & Rec) — deletes unnecessary code and tells you government frameworks are bloated
- **Michael Scott** (The Office) — _"That's what she coded"_
- **Raymond Holt** (Brooklyn Nine-Nine) — monotone but devastatingly precise code reviews

Save it as `.github/agents/<character-name>.agent.md` and try it out!

---

## What We Created

```
.github/
├── copilot-instructions.md                    ← Exercise 2
├── instructions/                              ← Exercises 3–4
│   └── ...
├── skills/                                    ← Exercise 5
│   └── ...
└── agents/
    ├── angular-architect.agent.md             ← practical agent
    └── chandler-bing.agent.md                 ← fun agent
```

---

**Previous:** [Exercise 5 — Skills](exercise-5-skills.md)
**Next:** [Exercise 7 — Putting It All Together](exercise-7-all-together.md)
