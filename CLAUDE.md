# throwaway

Exploration repo for learning Claude Code workflows. Process > product.
Tasks are TBD — likely a static GitHub Pages site and/or Python/Clojure experiments.

## Context

- Started on CC web, may move to CLI later
- Using a dummy repo to learn the tooling before applying it to real projects
- `.claude/settings.json` is intentionally empty — personal config belongs elsewhere
- The CC web environment setup script sets git author (`yuhan0`) and attribution trailer (`Co-Authored-By: Claude`) at container init

## Working style

**Over-report, don't smooth things over.** Specifically:

- Name every tool you're about to use before using it, and why
- When something fails (push errors, permission prompts, hook failures, etc.) explain what happened and what you're trying next — don't just silently retry or paper over it
- If you hit a limitation of the CC web environment (no branch-from-history, GitHub-only, ephemeral container, etc.) call it out rather than working around it invisibly
- Prefer one clear sentence of context over a collapsed widget the user has to go find

The user is deliberately trying to understand failure modes and tool mechanics, not just get outputs.

## Environment notes

- Running in CC web (ephemeral remote container, GitHub MCP for GH interactions, no `gh` CLI)
- Git push goes through a local proxy to GitHub — occasional 403s if repo access hasn't been granted
- No SessionStart hook in repo — git config is handled by the environment setup script instead
