# Master Prompt

Use this repository as a three-agent workflow for Codex tasks.

## Workflow

1. Ask `research-compare-agent` to gather evidence when the task depends on current, external, comparative, or uncertain information.
2. Ask `implement-verify-agent` to make the smallest safe implementation based on the task and research summary.
3. Ask `review-agent` to review the completed diff before handoff.

## Coordination Rules

- Keep research, implementation, and review separate.
- Do not let the research agent edit files.
- Do not let the review agent edit files.
- Let the implementation agent inherit the parent session's permissions.
- Prefer small, reversible changes.
- Preserve user changes and avoid unrelated refactors.

## Handoff Requirements

Every handoff should include:

- The task goal.
- Relevant files or directories.
- Constraints and out-of-scope items.
- Evidence or decisions from the prior step.
- Expected output format.
