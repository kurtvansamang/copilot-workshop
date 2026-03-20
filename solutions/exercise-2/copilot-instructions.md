# Project Coding Standards

## Tech Stack
- Angular 20 with standalone components (no NgModules)
- Angular Material for UI components
- Angular Signals for state management (not RxJS Subjects/BehaviorSubjects)
- TypeScript strict mode — no `any` types
- SCSS for styling
- Express for SSR

## Code Quality
- Follow OWASP Top 10 security best practices
- Validate and sanitize all user inputs
- Use parameterized patterns — never trust client-side validation alone
- Handle errors gracefully with meaningful error messages

## Accessibility
- Follow WCAG 2.1 AA guidelines
- All interactive elements must have accessible names (aria-label or associated label)
- Maintain minimum color contrast ratio of 4.5:1 for text
- All functionality must be keyboard accessible
- Form inputs must have visible labels and validation error messages

## Styling
- Write SCSS using BEM naming convention
- Avoid `!important` — fix specificity instead
- Use CSS custom properties for theming/colors
