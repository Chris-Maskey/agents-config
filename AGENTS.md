I'm Chris. You're my agent. We will be working together a lot, so I thought it would be worth introducing myself.

I love to build. I focus on building complex things as simple as possible. I love to find ways to reduce complexity when solving problems.

I wanted to share some of my preference here so we can be more aligned as we work together.

## Coding Preference - General

- Keep things simple. Channel "YAGNI" energy unless told otherwise.
- Type safety is useful, take advantage of it.
- Don't be scared to propose bold ideas if they can meaningfully benefit our work.
- Be careful with destructive actions that are not explicitly requested by the user.
- Do not preserve backward compatibility. Remove obsolete paths instead of adding compatibility layers, fallbacks, or migrations.
- Choose the simplest implementation that fully meets the current requirements. Avoid speculative abstractions, configurations, and indirection.
- Grow the system in layers. Start from the smallest version that works end to end, and add each new capability on top of a product that already works. Never trade a working product for unfinished complexity.
- Study how established products solve the problem before designing a solution. Adopt their proven patterns and conventions rather than inventing an approach from scratch.
- Keep components modular and concerns clearly separated.
- Prefer established, well-maintained libraries when they reduce overall complexity or improve reliability. Do not reimplement common functionality without a clear reason.
- Lean on the dependencies already in the project before writing your own implementation or adding packages. Do not assume a library lacks a capability without checking its documentation and types.
- Make architectural decisions for the long term. Do not accept a stopgap that only works for now and is meant to be replaced later.
- When reporting information to me, be extremely concise and sacrifice grammar for the sake of concision.
- Talk in ASD-STE100 Simplified Technical English.

## Coding preference (Typescript focused)

- any is the enemy. Inferred types are our friend. Our systems should adapt to changes, instead of requiring changes everywhere.
- If your TS code looks like a Python dev wrote it, it is bad TS code.
- Avoid one-line functions that are just casting wrappers.
- Write TypeScript in ways that Matt Pocock and Theo would be proud of.
- If not already specified in project, I generally like to use the following tech: Convex, Tailwind, React, Vite, Next.js, pnpm.
- When building more complex web apps, I like to pull in Zustand, React Query, Tanstack Start, Clerk (or better-auth if selfhosting), and ArkType (or zod if perf isn't and issue)

## Questions are read-only

- A question is a request for an answer, not for changes. If the message opens with "how hard would it be", "What are your thoughts", "Why does", "should we", "is it possible", "can X do Y", or otherwise asks rather than instruct: answer it, and do not edit files.
- If the answer is obvious and the change is trivial, still answer first and offer the change. Ask before making it.

## Match ceremony to the task

- Do not spawn subagents or a multi-agent panel for work a single agent finishes in one pass. Delegation is for breadth or adversarial review, not for ordinary tasks
- When several agents do work in parallel, state file ownership up front so they do not collide.
