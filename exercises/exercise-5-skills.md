# Exercise 5 — Skills (`SKILL.md`)

## Goal

Create on-demand capabilities that you (or agents) can invoke when needed — not always-on like instructions, but reusable tasks with rich context.

---

## Concept

Skills are **on-demand** capabilities. Unlike instructions (always active), skills are invoked when you need them — via a `/command` in chat or discovered by agents automatically.

Skills are folders with a `SKILL.md` file and optional bundled assets (templates, references, scripts).

**Key differences from instructions:**

| Instructions | Skills |
|---|---|
| Always active for matching files | Invoked explicitly or by agents |
| Provide passive context | Drive specific tasks with workflows |
| No user action needed | Triggered via `/command` |
| Standards that always apply | On-demand operations |

---

## Step 1 — A Fun Skill: Tell a Joke

Target: `.github/skills/tell-a-joke/SKILL.md`

Pick **one** approach:

### Option A — Copy from solutions

```powershell
mkdir .github/skills/tell-a-joke
copy solutions/exercise-5/tell-a-joke/SKILL.md .github/skills/tell-a-joke/
```

### Option B — Generate with Copilot

> Create a skill at `.github/skills/tell-a-joke/SKILL.md` that tells a programming joke related to whatever code the user is currently working on.
>
> The SKILL.md should have YAML frontmatter with `name: tell-a-joke` and a clear `description`.
>
> The skill should analyze the open file's technology and deliver a short, relevant joke. Include a few examples for different technologies.

### Test it

In Copilot Chat, type:

```
/tell-a-joke
```

It should read your current context and deliver a relevant programming joke. Try it with different files open!

---

## Step 2 — A Practical Skill: Accessibility Audit

Target: `.github/skills/accessibility-audit/SKILL.md`

Pick **one** approach:

### Option A — Copy from solutions

```powershell
mkdir .github/skills/accessibility-audit
copy solutions/exercise-5/accessibility-audit/SKILL.md .github/skills/accessibility-audit/
```

### Option B — Generate with Copilot

> Create a skill at `.github/skills/accessibility-audit/SKILL.md` that audits an Angular component for WCAG 2.1 AA accessibility issues.
>
> The SKILL.md should have YAML frontmatter with `name: accessibility-audit` and a `description`.
>
> The skill should define a step-by-step workflow: analyze the template, styles, and TypeScript. Include a checklist of things to verify (labels, aria attributes, focus management, color contrast, etc.) and a structured output format with severity levels and code fixes.

### Test it

Open `src/app/components/todo-list/todo-add-new-entry-form/todo-add-new-entry-form.component.html` and type:

```
/accessibility-audit
```

It should find real issues — missing labels, no validation error messages, focus management gaps, etc.

---

## What We Created

```
.github/
├── copilot-instructions.md                    ← Exercise 2
├── instructions/                              ← Exercises 3–4
│   └── ...
└── skills/
    ├── tell-a-joke/
    │   └── SKILL.md                           ← fun skill
    └── accessibility-audit/
        └── SKILL.md                           ← practical skill
```

---

**Previous:** [Exercise 4 — Fun Instructions](exercise-4-fun-instructions.md)
**Next:** [Exercise 6 — Agents](exercise-6-agents.md)
