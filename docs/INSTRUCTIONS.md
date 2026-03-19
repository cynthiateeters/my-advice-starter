# Instructions

This assignment has five parts. Work through them in order. Each part builds on the one before it.

---

## Part 1 — Plan your site with your agent

Before you touch this repo, you need a plan. You will create that plan by having a conversation with an AI agent in your **original** "What Should I...?" repo.

> **Model selection matters.** Copilot lets you choose which model your agent uses. You will see a multiplier next to each model — 0x (free), 1x, 3x, and higher. The higher the multiplier, the more capable the model, but the faster it burns through your premium request budget. A planning conversation is where model quality matters most. Spend the 1x or 3x here — one good planning conversation beats three mediocre ones. See [docs/guides/choosing-your-model.md](guides/choosing-your-model.md) for the full breakdown.

1. **Open your original "What Should I...?" repo** in VS Code
2. **Start a Copilot agent conversation** and send this exact message:

   > "Review the files in this repo. This was one of my first assignments in my JS class. Now I am being asked in a different assignment and a different repo to recreate this with brand new html/css/js. I want to create a prompt here using a markdown file you and I create after we plan together how that new site will be mine with my ideas and my design decisions. Then I will copy that file to the new repo and have an AI agent help me build that site."

3. **Watch the agent's first response carefully.**

   A **good** response looks like this — the agent read your files and named specific things it saw:

   > "Here's what I see from your workspace: `index.html` presents a form for users to select their vibe, duration, genre, and activity. The site is titled 'What Should I Listen To?' `data.js` contains an array of song options with properties: title, activity, vibe, genre, and duration..."

   A **bad** response looks like this — generic and could apply to any project:

   > "Great plan! Here's how we can proceed: 1. Review the current project. 2. Plan your new site. 3. Draft a markdown prompt..."

   If the agent gives you a generic response, push back. Tell it to read the files first and tell you specifically what it sees.

4. **The agent will ask you questions.** Answer them one at a time. If it asks too many questions at once, tell it to slow down and ask one question. If it tries to write the build prompt before you have made your design decisions, tell it you are not ready yet.

5. **When your planning conversation is complete**, the result is a file called `BUILD-PROMPT.md`. This file captures your design decisions and tells the next agent exactly what to build.

6. **Important: your data stays inside `BUILD-PROMPT.md`.** Any dataset, array, or object from your original repo should be included as a code block inside the build prompt — not copied as a separate file. No source files travel between repos. The build prompt is the only thing that crosses over.

7. **Copy `BUILD-PROMPT.md` into this repo** (your my-advice repo). You will use it in Part 3.

---

## Part 2 — Get it running

If you have already cloned this repo and run `npm install`, confirm everything still works and move on. If not, do it now.

1. **Clone this repo** and open it in VS Code
2. **Install dependencies:**
   ```bash
   npm install
   ```
   This also installs Husky, which sets up a pre-commit hook automatically.
3. **Start the dev server:**
   ```bash
   npm run dev
   ```
   Nothing will appear in the browser — that is expected. You haven't created any HTML files yet. Vite is running and ready for when you do.
4. **Confirm linting passes:**
   ```bash
   npm run lint
   ```
   This should pass with no errors. The `js/` folder only has a `.gitkeep` file right now, so there is nothing to lint.
5. **Confirm Husky is working:** Make a small test commit (like editing this file with a comment). When you commit, you should see lint-staged run in your terminal. If it does, Husky is installed correctly. You can revert this commit afterward if you like.

Once everything runs without errors, you are ready for Part 3.

---

## Part 3 — Build the site

Now you will use your build prompt to generate your site inside this repo.

1. **Make sure `BUILD-PROMPT.md` is in the root of this repo**
2. **Open this repo in VS Code agent mode**
3. **Paste the contents of `BUILD-PROMPT.md`** as your first message to the agent
4. The agent will generate files:
   - `index.html` in the repo root
   - JavaScript files in the `js/` folder (`data.js`, `matching.js`, `nav.js`, `app.js`)
5. **Run the linter:**
   ```bash
   npm run lint
   ```
   The agent may have introduced linting errors. Fix them — this is part of the learning. Read the error messages, understand what rule was violated, and check `docs/reference/eslint-rules.md` if you need help.
6. **Run the dev server:**
   ```bash
   npm run dev
   ```
   Confirm your page loads in the browser and test your form.

---

## Part 4 — Modify your AGENTS.md

Now that you have worked with an AI agent, you know more about what helps and what does not.

1. **Read `docs/a-good-agents-md.md`** — it explains what makes an effective AGENTS.md and how to write personal instructions
2. **Open `AGENTS.md`** in the repo root and scroll to the "My personal instructions" section at the bottom
3. **Add at least 3 personal instructions** based on your experience. Think about:
   - What did the agent do well that you want it to keep doing?
   - What did the agent do that was unhelpful?
   - How do you learn best — analogies, short examples, step-by-step?
   - Any design or code preferences specific to your project?
4. **Try them out.** Start a short conversation with the agent and see if your instructions change its behavior. Note what is different.

---

## Part 5 — Deploy and reflect

Wrap up by building, deploying, and reflecting on the process.

1. **Build the project:**
   ```bash
   npm run build
   ```
   Confirm Vite builds successfully with no errors.
2. **Deploy to Netlify using the Netlify CLI.** If you haven't set up the CLI yet, see the Netlify CLI guide on Canvas for installation and login steps. Then deploy:
   ```bash
   netlify deploy --prod
   ```
   Follow the prompts to link your repo to a new Netlify site. Save your live URL — you will submit it.
3. **Push to GitHub** and check the Actions tab — confirm the lint workflow runs and shows a green check
4. **Complete `ai-collaboration-summary-template.md`** — answer every question thoughtfully. This is where you reflect on what you learned about working with AI agents in a real tooling environment.

## What to submit

- Your live Netlify URL
- Your GitHub repo URL (make sure it is public or that your instructor has access)
- Your completed `ai-collaboration-summary-template.md` in the repo
