# AI Project Context Kit

**AI Project Context Kit** is a GitHub-ready starter structure for organizing AI project context, skills, instructions, templates, and task prompts as clean YAML files.

It helps you keep AI prompts smaller by loading only the context files and skills needed for a specific task instead of sending the whole project every time.

## About

This repository is an example of how to structure project knowledge for AI-assisted development.

Instead of one huge prompt, the project is split into:

- `context` — factual project information
- `instructions` — global AI rules and coding standards
- `skills` — reusable procedures for common tasks
- `templates` — reusable task/request formats
- `examples` — examples of correct output
- `tasks` — concrete tasks for the AI to execute or analyze
- `project-index.yaml` — main registry that connects contexts, skills, and rules

## Suggested GitHub repository settings

**Repository title:**

```txt
AI Project Context Kit
```

**About / Description:**

```txt
Starter YAML structure for AI-assisted software projects: clean context files, skills, instructions, templates, and task routing.
```

**Topics / Tags:**

```txt
ai, yaml, prompt-engineering, ai-workflow, context-engineering, software-architecture, developer-tools, workflow, llm, project-template
```

## Folder structure

```txt
ai-project-context-kit/
  ai/
    project-index.yaml
    context/
    instructions/
    skills/
    templates/
    examples/
    tasks/
  .github/
    ISSUE_TEMPLATE/
  README.md
  LICENSE
  .gitignore
  repository-metadata.yaml
```

## How it works

A task should not load all project information. It should load only the required contexts, instructions, and skills.

Example:

```yaml
task:
  title: Add users with roles
  type: full_feature

use:
  context:
    - project_overview
    - database_schema
    - api_spec
    - backend_architecture
    - frontend_architecture

  instructions:
    - global_rules
    - coding_rules
    - security_rules

  skills:
    - write_migration
    - add_api_endpoint
    - create_react_component
```

The AI or your own context loader can use `ai/project-index.yaml` to decide which files to include.

## Main idea

```txt
small task prompt
+ selected context files
+ selected skills
+ selected instructions
= cleaner AI request with fewer tokens
```

## Recommended workflow

1. Describe your project in `ai/context/`.
2. Put reusable AI behavior rules in `ai/instructions/`.
3. Put reusable procedures in `ai/skills/`.
4. Register everything in `ai/project-index.yaml`.
5. Create concrete task files in `ai/tasks/`.
6. For each AI request, load only the files required by the task.

## Example task

Open:

```txt
ai/tasks/add-users-roles.task.yaml
```

It shows how to connect one feature task to contexts, instructions, and skills.

## Example AI request

Open:

```txt
ai/tasks/sample-ai-request.md
```

It shows how to tell the AI that the attached YAML files are structured context, not a plain prompt.

## Notes

This is a template repository. Copy it into your own project and adjust the YAML files to your stack, database, API, UI, and coding standards.
