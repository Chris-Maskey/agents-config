---
name: plan-maker
description: Create clear, concise, agent-executable plans for work, projects, decisions, or changes when the user asks for a plan, roadmap, approach, milestones, or next steps.
---

# Plan Maker

Produce the smallest clear plan another agent can execute without inventing missing work.
Keep it concise; include only information that changes the route or verifies the result.

## 1. Define the destination

- State the outcome and scope in one sentence.
- State only assumptions or decisions that change the route.
- Ask one focused question only when its answer would change the route; otherwise choose and state a reasonable default.
- Complete when success and scope are clear to someone who did not join the discussion.

## 2. Inspect before prescribing

- For repository work, read the nearest `AGENTS.md`, relevant files, existing patterns, callers, tests, and configuration.
- For other work, inspect the supplied source material and constraints.
- Prefer existing paths, native capabilities, and deletion over new abstractions.
- Complete when every proposed step has a known target and no step rests on guesswork.

## 3. Build the route

- Order steps by dependency, not by file or team.
- Give each step an imperative action, exact target, and observable completion criterion.
- Combine steps that always change together; split steps that need separate decisions, owners, or checks.
- Make validation the final step.
- Complete when following the steps reaches the destination with no hidden prerequisite.

## 4. Resolve and present the plan

- If unresolved questions remain, invoke `grilling` with the plan and questions. Follow its rounds until its frontier is empty and the user confirms shared understanding.
- Fold the answers into the goal, assumptions, steps, and validation. Set `Unresolved questions: None`.
- If execution will continue in this session, update the steps with `update_plan` after folding in the answers.
- Invoke `html-communication` to render and publish the final plan.
- Use this shape:

  ```text
  Goal: <outcome and scope>
  Assumptions: <route-changing assumptions, or None>

  Steps:
  1. <action> — <exact target>. Done when: <observable result>.
  2. <action> — <exact target>. Done when: <observable result>.

  Validation: <check and expected result>
  Unresolved questions: <remaining questions, or None>
  ```

- End every plan with `Unresolved questions:` followed by the remaining questions, or `None`.
- Render the confirmed plan only after `Unresolved questions: None`.
- Planning-only requests end with the published HTML plan. Begin implementation only when the user also asks for execution.
- Complete when the final plan is published and the user can start step 1 without more planning.
