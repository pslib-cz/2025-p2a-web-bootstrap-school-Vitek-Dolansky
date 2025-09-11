# Copilot Instructions for AI Agents

## Project Overview
- This is a Vite-based static web project for SOŠ Digital, using Bootstrap 5 for UI components and custom styles in `src/style.css`.
- The main entry point is `src/main.js`, which sets up the app UI and imports Bootstrap and custom CSS.
- The project structure is flat, with all source files in `src/` and static assets in `public/` (if used).

## Key Files & Structure
- `index.html`: Main HTML template, includes Bootstrap via CDN and references `src/style.css`.
- `src/main.js`: App bootstrapper, imports Bootstrap CSS/JS and custom styles, sets up the main UI, and initializes the counter button using `setupCounter` from `src/counter.js`.
- `src/counter.js`: Exports `setupCounter(element)`, which attaches a click handler to increment a counter in the UI.
- `src/style.css`: Custom styles, overrides some Bootstrap defaults.
- Images and SVGs are in `src/` and referenced directly in HTML or JS.

## Developer Workflows
- **Development server:**
  ```sh
  npm run dev
  ```
  Starts Vite's dev server with hot reload.
- **Production build:**
  ```sh
  npm run build
  ```
  Outputs static files to `dist/`.
- **Preview build:**
  ```sh
  npm run preview
  ```
  Serves the production build locally.
- **Deploy:**
  ```sh
  npm run deploy
  ```
  Builds and deploys to GitHub Pages using `gh-pages`.

## Conventions & Patterns
- Use ES modules for all JS (`type: module` in `package.json`).
- Bootstrap is included both via CDN in `index.html` and as an npm dependency for local development.
- All custom JS should be placed in `src/` and imported via `main.js`.
- Images and static assets are referenced with relative paths from `src/` or `public/`.
- No framework-specific routing or state management; all navigation is handled via standard HTML/Bootstrap.

## Integration Points
- No backend or API integration; this is a purely static site.
- Deployment is handled via the `gh-pages` npm package.

## Examples
- To add a new interactive component, create a JS module in `src/` and import it in `main.js`.
- To customize styles, edit `src/style.css` or override Bootstrap classes.

---
For questions about project structure or workflows, see `package.json` scripts and the top-level `src/` directory for examples.
