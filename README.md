# AI Project Context Example

This example shows how to organize AI project context into separate clean files:

- `context/` — facts about the project
- `instructions/` — global AI rules
- `skills/` — reusable task procedures
- `templates/` — task/output templates
- `examples/` — examples of correct outputs
- `tasks/` — concrete task requests
- `project-index.yaml` — registry that links contexts, skills and instructions

Recommended usage:

1. Open `ai/project-index.yaml`.
2. Select only contexts and skills needed for the current task.
3. Send the task + selected files to AI.
4. Do not send the entire project context every time.

Core idea:

```text
short task prompt
+ required clean contexts
+ required skills
+ required instructions
= smaller and cleaner AI request
```
