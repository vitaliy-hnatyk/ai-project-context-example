# Contributing

Contributions are welcome.

## Rules

- Keep context files factual and reference-only.
- Put executable procedures in `ai/skills/`.
- Put global behavior rules in `ai/instructions/`.
- Register new files in `ai/project-index.yaml`.
- Keep YAML small and focused.

## Add a new context

1. Create a file in `ai/context/`.
2. Add `_meta.type: clean_context`.
3. Add `domain`, `role`, and `allowed_skills`.
4. Register it in `ai/project-index.yaml`.

## Add a new skill

1. Create a file in `ai/skills/`.
2. Add `_meta.type: skill`.
3. Add `scope.domains` and `requires_context`.
4. Register it in `ai/project-index.yaml`.
