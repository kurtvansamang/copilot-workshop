# Exercise 7 — Putting It All Together

## Goal

See how instructions, skills, and agents **work together** on a real feature. They don't compete — they stack.

---

## The Scenario

You need to add an **"edit todo"** feature. Here's how the layers complement each other:

### Layer 1 — Instructions (active automatically)

You don't need to do anything here — your instructions from earlier exercises are already active:

- Your **coding standards** ensure the new feature uses Signals, standalone components, BEM SCSS
- **Security instructions** ensure input validation
- **WCAG instructions** ensure the edit form is accessible

### Layer 2 — Pick an agent

Select the **Angular Architect** agent (from Exercise 6) and give it the task:

> Add an edit button to each todo card that opens a dialog to edit the title and description. The dialog should reuse the same form structure as the add-new-entry form.

The agent provides architecturally sound guidance, considering component reuse and state management patterns. The instructions layer provides the standards it follows automatically.

### Layer 3 — Run a skill

After the implementation is done, audit it with the accessibility skill:

```
/accessibility-audit
```

The skill checks your new feature against WCAG criteria and reports specific issues.

### Layer 4 — Fun code review

Switch to the **Chandler Bing** agent (or your own sitcom character) for a review:

> Review the edit feature I just added

Get a thorough (and entertaining) code review.

---

## Observe the Layers

| Layer | What It Does | How It Activates |
|---|---|---|
| **Instructions** | The rules | Passively — always on |
| **Agent** | The persona and expertise | You select it |
| **Skill** | A specific action | You invoke it (`/command`) |

They don't conflict. Instructions provide the baseline. Agents and skills build on top. The agent _reads_ the instructions. The skill _follows_ the instructions. Everything stacks.

---

**Previous:** [Exercise 6 — Agents](exercise-6-agents.md)
**Next:** [Exercise 8 — When to Use Which](exercise-8-decision-guide.md)
