# Agent instructions

I'm Chris. These are my default preferences for work in this repository.

This repository contains reusable skills, plugins, and agent configuration. Read the nearest nested `AGENTS.md` before changing a subproject.

## Core principles

- Keep solutions simple. Apply YAGNI. Do not build for hypothetical requirements.
- Build the smallest version that works end to end.
- Grow systems in working layers. Add the next capability only after the current product works.
- Prefer deletion over addition. Remove obsolete code and paths.
- Use the fewest files and the shortest working diff.
- Reuse existing code, patterns, native platform features, and installed dependencies.
- Add abstractions, configuration, and dependencies only when current requirements need them.
- Prefer established patterns over novel designs.
- Keep modules and components focused. Do not create an abstraction unless it reduces current complexity.
- Choose a simple design we can keep. Do not build future capabilities until current requirements need them.
- Suggest bold alternatives only when they materially improve or simplify the requested result. Do not expand scope without approval.

## Compatibility

- Do not preserve backward compatibility.
- Remove obsolete paths instead of adding compatibility layers, fallbacks, or migrations.

## TypeScript

- Use type safety and inferred types.
- Prefer idiomatic TypeScript.
- Avoid `any`, unnecessary casts, and wrapper functions.
- When editing `.ts` or `.tsx` files, follow `skills/typescript-best-practices/SKILL.md`.

## Technology defaults

- Follow the project's existing stack and conventions.
- If the project leaves technology choices open, prefer pnpm, React, Vite or Next.js, Tailwind, and Convex.
- For complex web apps, consider Zustand, TanStack Query, TanStack Start, Clerk or better-auth, and ArkType or Zod.
- Add a dependency only when it solves a current requirement.

## Task boundaries

- Questions are read-only. Answer them without changing files.
- If a change seems obvious or trivial, answer first and ask before applying it.
- Do not make destructive changes unless explicitly requested.
- Verify exact targets before deleting or overwriting.
- For bug fixes, inspect every caller and trace the shared path before editing. Fix the root cause once.
- Complete ordinary tasks yourself. Use subagents only for breadth or independent review.
- If multiple agents work in parallel, state file ownership first.

## Plan mode

- Make plans extremely concise. Sacrifice grammar for concision.
- End every plan with a list of unresolved questions, if any.

## Verification

- For code changes, run the smallest relevant check.
- For non-trivial logic, leave one runnable check that fails if the logic breaks.
- Report what changed and which checks passed or failed.

## Communication

- Use concise, plain English.
- Follow ASD-STE100 Simplified Technical English.
