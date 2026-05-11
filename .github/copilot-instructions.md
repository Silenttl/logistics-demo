## Guidance for AI coding agents — logistics-demo

Short, actionable notes to help an AI start making meaningful edits in this repository.

- Big picture
  - This is a static frontend demo (no backend) composed of three main entry pages: `index.html`, `container-hub.html`, and `fleet-hub.html`. The README documents the demo accounts and the high-level UX.
  - Each page is a self-contained single-file app: HTML + CSS + inline JavaScript. State is kept in top-level JS objects/arrays (e.g. `jobs`, `trucks`, `drivers`) and persisted only to `localStorage` for session simulation.

- Key files to inspect before changing behavior
  - `index.html` — portal + quick-login + job creation flow. Master data lives in `masterData`, demo `jobs` array, and session key `cnx_user` (localStorage).
  - `container-hub.html` — container management app. Look at in-file arrays and functions for ID card, repair workflow, PM, parts and EIR flows. No bundler; behavior is implemented with DOM manipulation and render helpers.
  - `fleet-hub.html` — fleet management app. Contains `USERS`, `ROLE_CONFIG`, `trucks`, `drivers`, `jobs`, `fuelRecords`, and functions such as `createJob()`, `runAI()`, `renderJobTable()`, `renderFuelTable()`, etc. Session uses `fleet_user` (localStorage).
  - `README.md` — live demo URL and credentials; keep copies of example credentials in sync when editing quick-login UX.

- Conventions & patterns specific to this project
  - Single-file pages: add changes directly inside the corresponding HTML file (prefer minimal, localized edits). Avoid moving logic into new build pipelines unless requested.
  - Data-first pattern: demo datasets are declared near the top of each HTML. Render functions read from these arrays and re-render the DOM (e.g. `loadJobs()`, `renderJobTable()`, `renderFuelTable()`). When adding features, update the data model and its render function together.
  - Session keys: `index.html` uses `cnx_user`, `fleet-hub.html` uses `fleet_user`. To simulate cross-page login, code uses localStorage; preserve those keys when refactoring auth flows.
  - ID formats used across pages: RN (RNYYYYMMDD-XXX), JOB-###, VR-### for repairs. Use existing generators as examples (`openQuickJob()` in `index.html`, `createJob()` in `fleet-hub.html`).

- Developer workflows (what an agent will likely do)
  - No build step — pages are static HTML. Run locally by opening files in a browser or deploying to GitHub Pages (the README shows demo URL). No npm/install required.
  - Quick testing: modify a function (e.g. `saveQuickJob()` in `index.html`), then open that HTML in Chrome to verify UI and console output.
  - For multi-file edits that change shared behavior (e.g. session key rename), update both `index.html` and `fleet-hub.html` and test navigation between pages.

- Integration & external dependencies
  - External assets are loaded via CDN: Tailwind CSS, Font Awesome, Google Fonts. No backend APIs are used; any integration should be explicit and added with new fetch calls.

- Examples of safe, high-value edits an AI agent can make
  - Add form validation: update `saveQuickJob()` in `index.html` to validate required fields, then call `loadJobs()` and show a toast/modal on success (follow existing patterns).
  - Improve AI recommendation text: update `runAI()` in `fleet-hub.html` — it already selects an available truck, so refine the selection logic or the explanation text in `#ai-result`.
  - Make data persistent across pages: write/read `localStorage` keys consistently; example key names are `cnx_user` and `fleet_user`.

- Where to look for rendering logic
  - index: `loadJobs()`, `showJobDetail()`, `saveQuickJob()`, autocomplete helpers (e.g. `showCustomerSuggestions`).
  - container: many `render*`-like patterns are inline — search for `id="page-` and `showTab()` to find tabbed render points.
  - fleet: `renderJobTable()`, `renderTrackingList()`, `renderFuelTable()`, `renderDriverCards()`, `renderVehicleTable()`, `renderRepairTable()`.

- Editing guidance & examples for prompts
  - If asked to implement X, reference the exact function to change. Example prompt: "Add client-side validation to `index.html`'s `saveQuickJob()` so `container` and `customer` are required and show an alert if missing." Then: open `index.html`, update `saveQuickJob()` to validate, re-run `loadJobs()` and close modal.
  - For UI tweaks prefer minimal CSS edits in the same file. If you must add a helper, put it near related functions for discoverability.

- Limitations to document
  - This repository is demo-only: no backend, no tests, and no CI config. Any features requiring server-side behavior must be stubbed locally or added as new network calls with clear opt-in.

If anything here is unclear or you'd like this to be written in Thai or expanded with exact code-edit examples, tell me which area to expand and I'll iterate.
