# cimpress-agentic-development

A shared project directory for Cimpress development teams to host app projects **and** the spec engineering artifacts that define standardized agentic development practices — reusable across organization domains.

## Why this repo exists

Every time a team ships a data product with agentic tooling (e.g. Cortex Code), they learn what works: how to structure the data, which Snowflake features to use, what prompts and workflows produce reliable results, and where the pitfalls are. Today that knowledge lives in individual heads and chat histories.

This repo captures it. Each project ships with two spec engineering artifacts:

| Artifact | Answers | Purpose |
|---|---|---|
| **Spec doc** (`SPEC.md`) | *What was built?* | Describes the product: problem, scope, architecture, data model, Snowflake objects, interfaces, decisions, and outcomes. |
| **Custom skill** (`skill/SKILL.md`) | *How was it built?* | Encodes the build workflow as a reusable Cortex Code skill — steps, gates, conventions, and lessons learned — so an agent can repeat it. |

The next team that ships a similar data product starts with full context: they read the spec, invoke the skill, and adapt rather than reinvent. **Every build gets faster than the last one**, turning individual best practices into organization-wide reusable knowledge.

## Repository layout

```
.
├── projects/                 # One folder per app / data product
│   └── <domain>-<project>/
│       ├── SPEC.md           # What was built
│       ├── skill/
│       │   └── SKILL.md      # How it was built (Cortex Code skill)
│       └── src/              # Application code, SQL, notebooks, etc.
├── skills/                   # Promoted, cross-domain reusable skills
├── templates/
│   ├── SPEC_TEMPLATE.md
│   └── SKILL_TEMPLATE.md
└── CONTRIBUTING.md
```

## Getting started

1. **Before building:** browse `projects/` and `skills/` for a similar product. Read its `SPEC.md` and install/invoke its skill.
2. **Start a new project:** copy the templates:
   ```bash
   mkdir -p projects/<domain>-<project>/{skill,src}
   cp templates/SPEC_TEMPLATE.md  projects/<domain>-<project>/SPEC.md
   cp templates/SKILL_TEMPLATE.md projects/<domain>-<project>/skill/SKILL.md
   ```
3. **While building:** keep the spec current and note decisions and gotchas.
4. **After shipping:** finalize the spec and skill (Cortex Code can help — e.g. "summarize this session as a skill"). Open a PR.
5. **Promote:** when a skill proves useful across domains, generalize it into `skills/`.

See [CONTRIBUTING.md](CONTRIBUTING.md) for conventions.
