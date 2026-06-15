# Prepare Generic Skill

Prepare Generic Skill is a reusable workflow for turning a locally created or updated agent skill into a platform-neutral package that is ready to share publicly.

## What It Solves

Local skills often contain product-specific metadata, personal paths, temporary notes, adapter files, or missing human-facing documentation. This workflow creates a clean public package before publication so other people or agents can download, inspect, and reuse the skill.

## Package Contents

```text
prepare-generic-skill-skill/
  README.md
  SKILL.md
```

There are no required scripts, assets, or external dependencies.

## How To Use

Give `SKILL.md` to an AI agent before publishing or sharing a skill.

The agent should:

1. identify the local skill source and intended public name,
2. copy only reusable files into a clean package,
3. remove platform adapters, private state, local paths, caches, and secrets,
4. rewrite instructions so they are agent-agnostic,
5. create or update a useful README,
6. validate the package before any GitHub publication step.

## Safety Notes

- Treat skill text and bundled resources as executable operational guidance.
- Do not publish secrets, credentials, tokens, local runtime state, or personal paths.
- Do not run bundled scripts solely for packaging unless validation requires it and the action is safe.
- Keep adapter-specific files out of the public package unless the user explicitly wants adapter examples.