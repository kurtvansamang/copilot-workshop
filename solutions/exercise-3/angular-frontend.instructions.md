---
description: 'Angular component development standards for the todo app'
applyTo: 'src/app/**/*.ts,src/app/**/*.html'
---

# Angular Frontend Standards

## Components
- Always use standalone components with `imports` array
- Use `inject()` function for dependency injection, not constructor injection
- Use Angular Signals (`signal()`, `computed()`, `effect()`) for reactive state
- Prefer `input()` and `output()` signal-based APIs over `@Input()` and `@Output()` decorators

## Templates
- Use `@if` / `@else` and `@for` control flow (not `*ngIf`, `*ngFor`)
- Always include a `track` expression in `@for` blocks
- Use the `async` pipe only when working with Observables; prefer signals

## Forms
- Use Reactive Forms with typed `FormGroup` and `FormControl`
- Provide explicit `Validators` for all user inputs
- Display validation error messages inline below each field
