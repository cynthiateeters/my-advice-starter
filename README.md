# My Advice

This repo gives you a fully configured professional tooling setup. Your job is to use an AI agent conversation to plan and build your personal "What Should I...?" site inside it.

The tooling is already here — linting, formatting, pre-commit hooks, CI, and a dev server. You bring the site.

## Getting started

```bash
npm install
npm run dev
```

After `npm install`, Husky sets up pre-commit hooks automatically. Running `npm run dev` starts the Vite dev server — nothing will appear in the browser yet because you haven't created your HTML files. That's expected.

## Learning objectives

- Set up and work inside a professional JavaScript tooling harness
- Understand what linting and formatting do and why teams use them
- Experience pre-commit quality gates that catch problems before they reach GitHub
- Read and understand a CI workflow with GitHub Actions
- Use an AI agent conversation to plan and generate a complete site from a build prompt

## File guide

Your docs folder has everything you need:

- [docs/INSTRUCTIONS.md](docs/INSTRUCTIONS.md) — step-by-step assignment walkthrough
- [docs/CHECKLIST.md](docs/CHECKLIST.md) — completion checklist for each part
- [docs/a-good-agents-md.md](docs/a-good-agents-md.md) — what makes an effective AGENTS.md
- [docs/tutorials/why-linting.md](docs/tutorials/why-linting.md) — what linting is and why it matters
- [docs/tutorials/how-husky-works.md](docs/tutorials/how-husky-works.md) — how pre-commit hooks work
- [docs/tutorials/github-actions-101.md](docs/tutorials/github-actions-101.md) — understanding CI with GitHub Actions
- [docs/reference/eslint-rules.md](docs/reference/eslint-rules.md) — every rule in this project explained
- [docs/reference/prettier-options.md](docs/reference/prettier-options.md) — formatting options reference
- [docs/reference/vite-vitest-basics.md](docs/reference/vite-vitest-basics.md) — what Vite and Vitest do
- [docs/guides/adding-features.md](docs/guides/adding-features.md) — stretch goals and extra features
- [docs/guides/modifying-context.md](docs/guides/modifying-context.md) — how to customize your AGENTS.md

## Where your site lives

The `js/` folder is where your generated site's JavaScript files will go. Your AI agent conversation will create files like `js/data.js`, `js/matching.js`, `js/nav.js`, and `js/app.js`.

The `index.html` file will be created by you via your Copilot agent conversation — it doesn't exist yet, and that's by design.
