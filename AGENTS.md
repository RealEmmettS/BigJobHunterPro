# Repository Guidelines

## Project Structure & Module Organization
The site is a static landing page. Core files live at the repo root:
- `index.html` for page markup and section layout.
- `styles.css` for global styling, variables, and responsive rules.
- `script.js` for animations, modal behavior, and effects.
- `imgs/` for screenshots and branding assets referenced by `index.html`.
- `README.md` and `concept.md` for product context and copy guidance.

## Build, Test, and Development Commands
No build system or package manager is configured.
- Local preview (recommended): `python -m http.server 8000` then open `http://localhost:8000`.
- Quick check: open `index.html` directly in a browser.

## Coding Style & Naming Conventions
- Indentation is 4 spaces in HTML, CSS, and JS.
- JavaScript uses semicolons and mostly single-quoted strings; keep functions in lowerCamelCase.
- CSS classes are kebab-case; keep new colors and shadows in `:root` variables.
- Asset names belong in `imgs/`; update references in `index.html` when renaming.

## Testing Guidelines
There are no automated tests yet.
- Manually verify modal open/close, counters, and scroll effects from `script.js`.
- Check responsive layout around 768px and 480px, matching the media queries in `styles.css`.

## Commit & Pull Request Guidelines
- Existing history uses short, sentence-case commit messages; keep messages concise and scoped.
- PRs should include a clear summary, screenshots for visual changes, and links to relevant issues or concepts.

## Security & Configuration Tips
- The site is static and contains no secrets; do not commit API keys or tracking tokens.
- If adding third-party scripts or analytics, document the change in `README.md` and keep sources pinned.
