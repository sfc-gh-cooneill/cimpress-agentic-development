# Contributing

## Project naming
`projects/<domain>-<project>` in lowercase kebab-case (e.g. `projects/print-ops-demand-forecast`).

## Definition of done
A project is not complete until it includes:
- [ ] `SPEC.md` filled out from `templates/SPEC_TEMPLATE.md`
- [ ] `skill/SKILL.md` filled out from `templates/SKILL_TEMPLATE.md`, tested by invoking it in Cortex Code
- [ ] Source code under `src/`, with no secrets or credentials committed

## Promoting a skill
When a project skill is reused by a second domain, generalize it (remove project-specific names, parameterize inputs) and move it to `skills/<skill-name>/SKILL.md`. Link back to the originating project specs.

## Pull requests
- One project (or one skill promotion) per PR.
- Reviewers check that the spec and skill agree with what the code actually does.
