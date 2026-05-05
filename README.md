# AgentCrew

AgentCrew is a lightweight, practical template for building **CrewAI-style multi-agent workflows**.

## CrewAI mental model in this repo

This project follows four core ideas:

1. **Agent**: a specialized worker with a role, goal, and optional tools.
2. **Task**: a unit of work assigned to a specific agent.
3. **Crew**: the orchestrator that wires agents and tasks together.
4. **Process**: how tasks run (sequential, hierarchical, or parallel).

## Why use AgentCrew

Use it when you want:

- decomposed workflows (research -> draft -> review)
- better output quality through specialization
- reusable team structures for repeated business or engineering tasks

Avoid it when:

- a single prompt is enough
- ultra-low latency is required
- fully autonomous operation must be guaranteed

## Example workflow shape

```text
Input Topic
  -> Research Agent task
  -> Writer Agent task
  -> Editor Agent task
  -> Final output
```

## Suggested starter crew

- **Researcher**: gathers facts and references
- **Writer**: produces first draft
- **Reviewer**: checks quality, style, and consistency

## Next steps

- Add agent definitions under `agents/`
- Add task definitions under `tasks/`
- Add orchestration entrypoint under `crew.py`
- Add tests for each workflow stage
