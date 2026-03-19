# Netlify CLI cheat sheet

OUTLINE — not yet written

## Purpose

Quick-reference for the commands students actually use in this project. No explanation of why — that lives in the Canvas tutorial. This is the card you tape to your monitor.

## Sections

### Install
- `npm install -g netlify-cli`
- Verify: `netlify --version`

### Login
- `netlify login` — opens browser, authorizes, done
- One-time setup

### Link your repo to a Netlify site
- `netlify init` — first time, connects this repo to a new Netlify site
- `netlify link` — reconnect if you cloned fresh or switched machines
- `netlify status` — confirm you're linked and who you're logged in as

### Deploy
- `netlify deploy` — draft deploy (preview URL, not live)
- `netlify deploy --prod` — production deploy (your real URL)
- Both deploy the `dist/` folder after you run `npm run build`

### Local dev
- `netlify dev` — runs Vite dev server with Netlify features (serverless functions, redirects)
- Matters in Week 7 when the chatbot uses a serverless function

### Useful extras
- `netlify open` — opens your site's Netlify dashboard in the browser
- `netlify logout` — if you need to switch accounts

## Tone notes
- Match eslint-rules.md and prettier-options.md style: short entries, command + what it does, no paragraphs
- Every entry should be copy-pasteable
