---
description: 'SCSS and styling standards for the todo app frontend'
applyTo: '**/*.scss'
---

# SCSS Styling Standards

## Naming
- Use BEM convention: `.block__element--modifier`
- Component host selectors should use `:host` sparingly

## Rules
- Never use `!important` — fix specificity or restructure selectors
- Use CSS custom properties (`var(--color-primary)`) for themed values
- Keep nesting to a maximum of 3 levels deep
- Use `rem` or `em` units for font sizes and spacing — avoid `px` for font sizes
- Ensure focus styles are visible (never `outline: none` without a replacement)
