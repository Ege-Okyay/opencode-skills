---
name: readme-writing
description: "Use when creating or improving a README — project summary, quickstart, install and usage examples, configuration reference, troubleshooting, contributing and license sections, and verifying commands actually work."
license: MIT
---

# README Writing

A README's job: in under a minute, a stranger knows what the project
does, whether it fits their need, and how to try it.

## When to Use This Skill
- New repository or package
- Issues keep asking the same setup questions
- README describes an older version of the project

## Structure
1. **Name + one-sentence description** — what it is and who it's for.
2. **Why / key features** — 3–5 bullets, concrete.
3. **Quickstart** — the shortest path to something working.
4. **Usage** — common tasks with copy-pasteable examples and real output.
5. **Configuration** — table of options, env vars, defaults.
6. **Development** — clone, install, test, lint.
7. **Troubleshooting / FAQ** — the top recurring issues.
8. **Contributing, license, links** to full docs.

## Quickstart template
````markdown
## Quickstart

Requires Node 20+.

```bash
npm install acme-cli
npx acme init my-app
cd my-app && npx acme dev
```

Open http://localhost:3000 — you should see the welcome page.
````

## Configuration table
| Variable | Default | Description |
|----------|---------|-------------|
| `PORT` | `3000` | HTTP port |
| `DATABASE_URL` | — (required) | Postgres connection string |

## Writing rules
- Lead with what the user gets, not the implementation.
- Every command must be runnable as written; test them in a clean environment.
- State prerequisites and versions up front.
- Show expected output so readers know it worked.
- Use relative links to docs in the repo so they work on forks.
- Put long reference material in `docs/`, link from the README.
- Add a screenshot or GIF for visual tools.

## Keeping it current
- Update the README in the same PR as the behaviour change.
- Run README commands in CI where feasible (e.g., a docs smoke test).
- Remove sections rather than leaving them wrong.

## Avoid
- Wall-of-badges headers that push content below the fold
- "Simply" / "just" — nothing is simple for someone new
- Marketing claims without examples
