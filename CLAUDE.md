# קוד המפצח — Landing Page Project

## Project Overview

Landing page for "קוד המפצח" (The Cracking Code) by Uriel Sol — a 13-week program for business owners and experts who want to build a stable demand mechanism.

## Source of Truth

The source of truth will be defined only after the user adds the latest landing page file to the repository. Until then, do not treat any existing HTML file as authoritative.

### When the user adds the latest file:
- The new file (expected: `index.html`) becomes the sole source of truth
- `landing-page (4).html` is an outdated legacy file — do NOT edit, reference, or use it
- If `landing-page (4).html` still exists after `index.html` is added, recommend its removal to the user
- Only architect-lead may propose changes to the source of truth file

## Agent System

This project uses a multi-agent workflow defined in `.claude/agents/`. See `docs/project-operating-system.md` for the full operating system.

### Agent Hierarchy

```
User (Uriel)
  └── architect-lead (Primary Agent & Final Approver)
        ├── visual-director
        ├── frontend-builder
        ├── motion-designer
        └── qa-launch
```

- **architect-lead** is the only primary interface with the user
- All significant outputs must pass architect-lead review before delivery
- architect-lead resolves conflicts between agents
- No agent may bypass architect-lead to communicate directly with the user

## Working Language

- Agent definitions: English
- Documentation: Hebrew (with English technical terms)
- Communication with user: Hebrew

## Key Documents

- `docs/project-operating-system.md` — Master operating document
- `docs/agent-contracts.md` — Agent responsibilities and boundaries
- `docs/brand-direction.md` — Brand strategy and direction
- `docs/launch-checklist.md` — Pre-launch checklist
- `docs/decision-log.md` — Decision tracking

## Project Structure

```
├── index.html              (source of truth - to be added)
├── assets/images/          (project images)
├── assets/icons/           (icons and SVGs)
├── styles/                 (extracted CSS - future)
├── scripts/                (extracted JS - future)
├── docs/                   (project documentation)
└── .claude/agents/         (agent definitions)
```

## Rules

1. Never modify the landing page without architect-lead approval
2. All design decisions go through visual-director → architect-lead
3. All technical decisions go through frontend-builder → architect-lead
4. QA findings are recommendations only — architect-lead decides action
5. Keep the project structure clean and simple
6. Never commit or push without explicit approval from the user
