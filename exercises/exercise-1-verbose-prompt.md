# Exercise 1 — The Verbose Prompt

## Goal

Experience the problem firsthand: adding the same context to every prompt gets old fast.

---

## The Problem

Open Copilot Chat and ask it to add a "due date" field to the todo app. But you want it done _right_, so you include all the context:

### Try this prompt:

> Add a "due date" field to the Todo model and the add-new-entry form. The due date should be optional. Use Angular Material's datepicker component.
>
> Follow these rules:
> - Use Angular Signals for state management (this project uses signals, not RxJS)
> - Use standalone components (no NgModules)
> - Follow WCAG 2.1 AA accessibility guidelines: proper labels, aria attributes, keyboard navigation, color contrast 4.5:1
> - Follow OWASP security best practices: validate inputs, sanitize data, don't trust client-side validation alone
> - Write SCSS following BEM naming conventions, avoid using !important
> - Use Angular reactive forms with proper validators
> - Add meaningful form validation error messages visible to the user
> - Use TypeScript strict mode, no `any` types

That's a _huge_ prompt for a simple feature. And you'd need to repeat most of it for every subsequent request.

---

## What to Observe

1. The response should follow most of your rules — good!
2. Now ask a follow-up: **"Also add a priority dropdown (low/medium/high)"** — notice that Copilot might forget some of your rules since they're not in this new prompt
3. You'd have to paste the whole context block _again_

---

## The Takeaway

> **This is the problem we're going to solve.** In the next exercises, we'll extract these rules into customization files so you never have to repeat them.

---

**Previous:** [Exercise 0 — Explore the App](exercise-0-explore-the-app.md)
**Next:** [Exercise 2 — Project-Level Instructions](exercise-2-project-instructions.md)
