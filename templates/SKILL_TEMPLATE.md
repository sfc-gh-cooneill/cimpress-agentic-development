---
name: <skill-name>
description: <One or two sentences on what this skill builds and when to use it.> Triggers: <keyword>, <keyword>.
---

# <Skill Name>

Encodes how <project> was built so it can be repeated for similar data products.

## When to use
- <situation>

## Inputs to gather
Ask the user for (use defaults where sensible):
- Source database/schema
- Target database/schema
- Warehouse and role

## Workflow

### Step 1: <Discover / assess>
<What to inspect and why.>

**Gate:** confirm findings with the user before continuing.

### Step 2: <Build data layer>
<Objects to create, conventions to follow.>

### Step 3: <Build app / agent / interface>

### Step 4: <Validate>
<Checks, tests, expected results.>

### Step 5: <Document>
Update the project `SPEC.md` with what was built.

## Conventions
- Naming:
- Roles/grants:

## Lessons learned / pitfalls
- <gotcha and how to avoid it>

## References
- Spec: `../SPEC.md`
