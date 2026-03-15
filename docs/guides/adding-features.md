# Adding features

Once your site is running and linting passes, try one of these tiers to push your skills further.

---

## Comfortable

**Add a second Vitest test for an existing function.**

Your `js/matching.js` file has logic functions that filter or match data. Write a test that imports one of those functions and checks that it returns the correct result for a specific input.

Create a file called `js/matching.test.js`:

```js
import { describe, it, expect } from "vitest";
import { yourFunction } from "./matching.js";

describe("yourFunction", () => {
  it("should return the expected result for a known input", () => {
    const result = yourFunction(/* your test input */);
    expect(result).toEqual(/* your expected output */);
  });
});
```

Run it with `npm run test`. Replace `yourFunction` with an actual function from your matching logic.

---

## Stretching

**Add a results page with shared navigation.**

If your agent only generated one page, add `results.html` as a second page. Then use `js/nav.js` to inject a shared navigation bar into both pages.

The nav injection pattern:

```js
// js/nav.js
const nav = `
  <nav>
    <a href="/">Home</a>
    <a href="/results.html">Results</a>
  </nav>
`;

const header = document.querySelector("header");
if (header) {
  header.innerHTML = nav;
}
```

Import `nav.js` in both HTML files with a `<script type="module">` tag. This way, you update navigation in one place and it appears on every page.

---

## Adventurous

**Write a Vitest test that mocks the DOM.**

Test that `app.js` displays the right number of results when given specific data. This requires setting up a minimal DOM in your test.

```js
import { describe, it, expect } from "vitest";

describe("results display", () => {
  it("should show the correct number of result cards", () => {
    // Set up a minimal DOM
    document.body.innerHTML = '<div id="results"></div>';

    // Import and run your display function
    // Check that the right number of elements were created
    const cards = document.querySelectorAll("#results .card");
    expect(cards.length).toBe(/* expected count */);
  });
});
```

This is advanced. The `jsdom` environment in Vitest makes it possible — your test file runs with a simulated browser DOM. If you get stuck, that is normal. Ask your agent for help and pay attention to how it explains the DOM testing pattern.
