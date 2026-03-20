# Exercise 2 — Project-Level Instructions (`copilot-instructions.md`)

## Goal

Stop repeating yourself. Extract the rules from Exercise 1 into a file Copilot reads automatically.

---

## Concept

Instructions are markdown files that Copilot reads **automatically** — no need to paste rules into every prompt.

The simplest form is a single file at `.github/copilot-instructions.md` that applies to **everything** in the project.

---

## Step 1 — Create the file

Target: `.github/copilot-instructions.md`

Pick **one** of these approaches:

### Option A — Copy from solutions

Copy the ready-made file:

```powershell
mkdir .github
copy solutions/exercise-2/copilot-instructions.md .github/copilot-instructions.md
```

### Option B — Generate with Copilot (recommended!)

Open Copilot Chat and use this prompt (feel free to tweak it):

> Analyze this Angular project's architecture, dependencies, and code patterns. Generate a `.github/copilot-instructions.md` file with project-level coding standards covering:
> - The tech stack and framework conventions (based on what you find in the codebase)
> - OWASP security best practices
> - WCAG 2.1 AA accessibility requirements
> - SCSS/styling conventions
>
> The instructions should apply to every Copilot interaction in this project.

Copilot will analyze the actual codebase and generate rules tailored to it. Review what it produces — you might want to adjust or add things!

## Step 2 — Test it

Now **restart Copilot Chat** (close and reopen the panel) and ask the **same feature request**, but shorter:

> Add a "due date" field to the Todo model and the add-new-entry form using Material datepicker. The due date should be optional.

### What to observe:

- Copilot now follows your standards **without you listing them**
- It should use Signals, standalone components, proper accessibility, BEM SCSS, etc.
- Ask the follow-up _"Also add a priority dropdown"_ — the rules persist!

---

## Why This Works

The `copilot-instructions.md` file is automatically included as context for **every** Copilot interaction in this project. You write the rules once; Copilot reads them always.

---

## What We Created

```
.github/
└── copilot-instructions.md   ← always-on, applies to everything
```

---

**Previous:** [Exercise 1 — The Verbose Prompt](exercise-1-verbose-prompt.md)
**Next:** [Exercise 3 — Scoped Instructions](exercise-3-scoped-instructions.md)
