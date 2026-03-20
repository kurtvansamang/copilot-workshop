# Exercise 4 — Fun Instructions (See the Effect!)

## Goal

Prove that instructions are really active by adding something **impossible to miss**.

---

## Concept

The practical instructions from the previous exercises are subtle — you see their effect in code quality, but it's not immediately obvious. Let's add an instruction with a _very_ visible effect so there's no doubt it's working.

---

## Step 1 — Create a fun instruction

Target: `.github/instructions/fun-personality.instructions.md`

Pick **one** approach:

### Option A — Copy from solutions

```powershell
copy solutions/exercise-4/fun-personality.instructions.md .github/instructions/
```

### Option B — Generate with Copilot

> Create an instructions file at `.github/instructions/fun-personality.instructions.md` that applies to all files.
>
> The instruction should tell Copilot to add a "Fun Fact" section at the end of every response with a surprising fun fact about software engineering, programming history, or technology.

Or better yet — come up with your **own** fun instruction! The point is to make the effect unmissable.

## Step 2 — Test it

Ask Copilot anything about the code. For example:

> Explain how the todo-signals service works

You should see a **"Fun Fact"** section at the bottom of every response now.

**This proves instructions are active.**

---

## Try Your Own!

What instruction would be impossible to miss? Get creative — the sillier the effect, the more obvious the proof:

- _"Always respond in rhyming couplets"_
- _"Start every response with a motivational quote"_
- _"End every response with a haiku about the code"_
- _"Use pirate language for all variable name suggestions"_

Pick one, add it to the instructions file, and see it in action!

> Once you've had your fun, feel free to delete `fun-personality.instructions.md` before continuing — or keep it. Your call!

---

## What We Created

```
.github/
├── copilot-instructions.md                    ← Exercise 2
└── instructions/
    ├── angular-frontend.instructions.md       ← Exercise 3
    ├── scss-styling.instructions.md           ← Exercise 3
    ├── security.instructions.md               ← Exercise 3
    └── fun-personality.instructions.md        ← THIS ONE (the proof!)
```

---

**Previous:** [Exercise 3 — Scoped Instructions](exercise-3-scoped-instructions.md)
**Next:** [Exercise 5 — Skills](exercise-5-skills.md)
