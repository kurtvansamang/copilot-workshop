# Exercise 0 — Explore the App

## Goal

Get familiar with the todo app codebase before we start customizing Copilot.

---

## What to Do

Open the project in `angular-todo-list/`. Take a quick look around:

- It's an **Angular 20** todo app with **Angular Material**, **Signals** for state management, and **SSR**
- Components are in `src/app/components/todo-list/`
- State lives in `src/app/services/todo-signals.service.ts`
- There's a `Todo` model in `src/app/models/model/todo.model.ts`

You can run it:

```bash
cd angular-todo-list
npm install
npx ng serve
```

## Quick Observations

Take note of these — they will matter in later exercises:

- **No WCAG/accessibility** considerations (missing labels, focus management, color contrast)
- **A validation bug** in `todo-signals.service.ts` (`|| undefined` always truthy)
- **Excessive `!important`** in SCSS files
- **No input length limits**, no error messages shown to users
- **localStorage data parsed** without error handling

These are exactly the things you'd want Copilot to fix — and exactly the context you'd keep repeating in prompts.

---

## Key Files to Browse

| File | What's There |
|---|---|
| `src/app/components/todo-list/todo-card/todo-card.component.ts` | Main card component with Signals |
| `src/app/components/todo-list/todo-add-new-entry-form/` | The add-todo dialog form |
| `src/app/services/todo-signals.service.ts` | Signal-based state management |
| `src/app/models/model/todo.model.ts` | The Todo model class |
| `src/app/components/todo-list/todo-card/todo-card.component.scss` | Lots of `!important` |

---

**Next:** [Exercise 1 — The Verbose Prompt](exercise-1-verbose-prompt.md)
