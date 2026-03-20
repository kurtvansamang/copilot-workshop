# Exercise 3 — Scoped Instructions (`.instructions.md`)

## Goal

Apply different rules to different parts of the codebase. A .NET backend doesn't need SCSS rules, and test files need different guidance than production code.

---

## Concept

Scoped instructions use the `applyTo` frontmatter field to target specific files via glob patterns. When Copilot works on a file matching the pattern, that instruction applies automatically.

---

## Step 1 — Angular Frontend Instructions

Target: `.github/instructions/angular-frontend.instructions.md`

Pick **one** approach:

### Option A — Copy from solutions

```powershell
mkdir .github/instructions
copy solutions/exercise-3/angular-frontend.instructions.md .github/instructions/
```

### Option B — Generate with Copilot

> Analyze the Angular components in `src/app/`. Generate an instructions file at `.github/instructions/angular-frontend.instructions.md` with Angular best practices.
>
> It should have YAML frontmatter with `applyTo: 'src/app/**/*.ts,src/app/**/*.html'` and a `description`.
>
> Cover: standalone component conventions, Angular Signals usage, modern control flow syntax, reactive forms best practices. Base the rules on what Angular 20 recommends.

This is a great one to generate — Copilot knows Angular best practices well and can tailor them to the actual code patterns in the project.

---

## Step 2 — SCSS Styling Instructions

Target: `.github/instructions/scss-styling.instructions.md`

Pick **one** approach:

### Option A — Copy from solutions

```powershell
copy solutions/exercise-3/scss-styling.instructions.md .github/instructions/
```

### Option B — Generate with Copilot

> Look at the SCSS files in this project. Generate an instructions file at `.github/instructions/scss-styling.instructions.md` with SCSS best practices.
>
> Use `applyTo: '**/*.scss'` in the frontmatter.
>
> Cover: BEM naming, avoiding !important, CSS custom properties, nesting limits, accessible focus styles. Address the specific issues you see in the existing SCSS files.

---

## Step 3 — Security Instructions

Target: `.github/instructions/security.instructions.md`

Pick **one** approach:

### Option A — Copy from solutions

```powershell
copy solutions/exercise-3/security.instructions.md .github/instructions/
```

### Option B — Generate with Copilot

> Generate an instructions file at `.github/instructions/security.instructions.md` with OWASP security best practices relevant to an Angular + TypeScript web application.
>
> Use `applyTo: '**'` in the frontmatter so it applies to all files.
>
> Cover: input validation, sanitization, safe JSON parsing, localStorage security, strict typing. Look at the existing code for specific security concerns to address.

## Step 4 — Test the scoping

1. Open `src/app/components/todo-list/todo-card/todo-card.component.ts` and ask Copilot to refactor it — the **Angular frontend instructions** should apply
2. Open a `.scss` file and ask Copilot to fix the styling — the **SCSS instructions** kick in
3. Open the service file and ask about localStorage handling — the **security instructions** guide the response

---

## Key Insight

Different files get different context, automatically. Frontend devs and backend devs in the same repo each get relevant guidance. In a real-world project you might have:

- `applyTo: '**/*.cs'` → C# / .NET conventions
- `applyTo: '**/*.ts,**/*.html'` → Angular conventions
- `applyTo: '**/*.spec.ts'` → Testing guidelines
- `applyTo: '**'` → Universal rules (security, general quality)

---

## What We Created

```
.github/
├── copilot-instructions.md                    ← Exercise 2
└── instructions/
    ├── angular-frontend.instructions.md       ← scoped to TS/HTML
    ├── scss-styling.instructions.md           ← scoped to SCSS
    └── security.instructions.md               ← scoped to everything
```

---

**Previous:** [Exercise 2 — Project-Level Instructions](exercise-2-project-instructions.md)
**Next:** [Exercise 4 — Fun Instructions](exercise-4-fun-instructions.md)
