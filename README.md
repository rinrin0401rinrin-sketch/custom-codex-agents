# custom-codex-agents

Project-specific Codex subagent prompts for a three-step workflow:

1. Research and compare evidence.
2. Implement focused changes and verify them.
3. Review the result before handoff.

## Structure

```text
custom-codex-agents
├─ README.md
├─ agents/
│  ├─ research-compare-agent.md
│  ├─ implement-verify-agent.md
│  └─ review-agent.md
└─ prompts/
   ├─ master-prompt.md
   └─ work-prompt.md
```

## Agents

- `research-compare-agent.md`: Research-only role for official sources, related institutions, competitor examples, and comparison evidence.
- `implement-verify-agent.md`: Implementation role for focused code changes and relevant verification.
- `review-agent.md`: Final review role for correctness, regressions, missing tests, security, maintainability, and request fit.

## Recommended Flow

1. Start with `prompts/master-prompt.md` to explain the overall collaboration pattern.
2. Use `prompts/work-prompt.md` for each concrete task.
3. Run the agents in order: research, implementation, review.
