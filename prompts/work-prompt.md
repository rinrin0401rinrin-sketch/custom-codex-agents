# Work Prompt

Use this prompt for a concrete task.

## Task

Describe the requested change or investigation here.

## Step 1: Research

Use `agents/research-compare-agent.md`.

Ask for:

- Official sources and URLs.
- Related institutions or standards.
- Competitor or similar examples.
- Risks, unknowns, and implementation recommendation.

## Step 2: Implement

Use `agents/implement-verify-agent.md`.

Provide:

- The task goal.
- The research summary.
- Target files or likely areas.
- Constraints and non-goals.

Ask for:

- Smallest safe diff.
- Relevant tests or checks.
- Remaining risks.

## Step 3: Review

Use `agents/review-agent.md`.

Ask for:

- Verdict.
- Critical and important issues.
- Missing tests or verification gaps.
- Final recommendation.
