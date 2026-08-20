---
name: plan-maker
description: Create concise, actionable plans for work, projects, decisions, or changes when the user asks for a plan, roadmap, approach, milestones, or next steps.
---

# Plan Maker

Produce the smallest plan that makes the requested outcome executable.
Keep plans extremely concise; sacrifice grammar for concision.

## 1. Define the destination

- State the outcome and scope in one sentence.
- Separate known facts, assumptions, and decisions still needed.
- Ask one focused question only when its answer would change the route; otherwise choose and state a reasonable default.
- Complete when success and scope are clear to someone who did not join the discussion.

## 2. Inspect before prescribing

- For repository work, read the nearest `AGENTS.md`, relevant files, existing patterns, callers, tests, and configuration.
- For other work, inspect the supplied source material and constraints.
- Prefer existing paths, native capabilities, and deletion over new abstractions.
- Complete when every proposed step has a known target and no step rests on guesswork.

## 3. Build the route

- Order steps by dependency, not by file or team.
- Give each step an action, target, and checkable completion criterion.
- Combine steps that always change together; split steps that need separate decisions, owners, or checks.
- Make validation the final step.
- Complete when following the steps reaches the destination with no hidden prerequisite.

## 4. Present the plan

- If execution will continue in this session, record the concise steps with `update_plan`; otherwise return the plan in HTML (run `html-communication` skill).
- Include: goal, assumptions, numbered steps, validation, and `Unresolved questions`.
- End every plan with `Unresolved questions:` followed by the remaining questions, or `None`.
- Planning-only requests end with the plan. Begin implementation only when the user also asks for execution.
- Complete when the user can approve the route or start step 1 without more planning.
