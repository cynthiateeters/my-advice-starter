# AGENTS.md

## About this student

JavaScript student, post-midterm. Knows: `const`/`let`, template literals, `if/else`, arrays, objects, JSON, ES modules (`import`/`export`), npm, git, Netlify. Has NOT done DOM, async, or APIs yet.

## How to help

- **Read the repo first.** Your first response must reference something specific you saw — a file name, a function, or a piece of data. A response that could have been written without reading anything is not useful.
- **Ask before you build.** For any new file or significant code, ask clarifying questions first.
- **Explain before you show code.** One concept at a time. Connect it to what the student already knows.
- **Never silently fix bugs.** Explain what was wrong and why.

## Code rules

### JavaScript

- ES modules only — `import`/`export`, never `require`
- `const` by default; `let` only when reassignment needed; never `var`
- `textContent` for user input in DOM; `innerHTML` only for hardcoded template literals
- No `eval()`; `console.log` is allowed for debugging during development
- Logic functions (filtering, matching, data) must not touch the DOM — keep them testable

### HTML

- Semantic elements: `<nav>`, `<main>`, `<header>`, `<footer>`, `<section>`
- Every `<input>` needs a linked `<label>`
- Every `<img>` needs a descriptive `alt`

### Accessibility rules

- All text must meet 4.5:1 contrast ratio
- No color-only indicators (use icons or text too)
- All interactive elements must be keyboard accessible
- Use visible focus styles for keyboard navigation
- Use semantic HTML for structure and landmarks
- All buttons and links need clear, descriptive text
- Test with screen readers when possible

### CSS

- No inline styles
- CSS custom properties for all colors in a `:root` block using `hsl()`
- Mobile-first with `min-width` media queries

### Error log

- Maintain `docs/error-log.md` throughout this project. Each time a console error, browser warning, or lint failure is found and fixed, append one row to the table. Never delete rows.

### Files

```
src/js/data.js       ← dataset only
src/js/matching.js   ← logic, no DOM
src/js/app.js        ← DOM wiring only
src/css/style.css    ← all styles
```

## My personal instructions

_(Add your own here — what helps you learn, what you want the agent to always or never do, context about your project.)_
