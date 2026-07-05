# Project Issues (Task Board)

This issue board represents the modular breakdown of the **Byte True Personal Website** project. Each issue is independently grabbable, self-contained, and describes a specific deliverable.

---

## Issue 001: Configure Astro Skeleton & Tailwind v4 Custom M-Design Theme
*   **Status**: `COMPLETED`
*   **Description**: Initialize an Astro static project, set up Tailwind CSS v4 using `@tailwindcss/vite`, configure custom theme variables (`--color-canvas`, `--color-m-blue-light`, `--color-m-red`, custom weights for Inter) to establish the brand design.
*   **Deliverables**:
    *   `package.json` with correct dependencies.
    *   `astro.config.mjs` with `@tailwindcss/vite` plugin.
    *   `src/styles/global.css` containing custom `@theme` tokens and base styles.

---

## Issue 002: Implement Global Layout & Brand Chrome Components
*   **Status**: `COMPLETED`
*   **Description**: Create the global wrapper `Layout.astro` and fundamental visual chrome components: the 64px `TopNav`, the minimalist footer, and the signature 4px tricolor M-Stripe.
*   **Deliverables**:
    *   `src/components/MStripeDivider.astro`
    *   `src/components/TopNav.astro`
    *   `src/components/Footer.astro`
    *   `src/layouts/Layout.astro`

---

## Issue 003: Implement Home Page (Profile, Philosophy & Workbench)
*   **Status**: `COMPLETED`
*   **Description**: Implement `src/pages/index.astro` displaying the full-bleed Hero image header, a two-column "Philosophy" section, a "Workbench" grid for projects with `spec-cell` styling, and a preview grid for the technical journal.
*   **Deliverables**:
    *   `src/pages/index.astro`
    *   Integration with Astro Content Collections (`projects` and `blog`).

---

## Issue 004: Implement Blog List Page & Dynamic Post Detail Routing
*   **Status**: `COMPLETED`
*   **Description**: Create the journal listing page displaying posts in `magazine-article-card` grids, and a dynamic router page `[...slug].astro` for rendering Markdown posts. Set up local CSS styles inside `src/styles/global.css` to format headings, blockquotes, lists, and code blocks for pristine code readability.
*   **Deliverables**:
    *   `src/pages/blog/index.astro`
    *   `src/pages/blog/[...slug].astro`
    *   `.article-content` CSS formatting rules in `src/styles/global.css`.

---

## Issue 005: Author Initial Content (Democratization Essay & Project Schema)
*   **Status**: `COMPLETED`
*   **Description**: Create schemas in `src/content.config.ts`. Author the initial metadata for the `u2wda-mcp` project in json, and write the inaugural Chinese philosophical essay `tech-democratization.md` on Tech Democratization.
*   **Deliverables**:
    *   `src/content.config.ts`
    *   `src/content/projects/u2wda-mcp.json`
    *   `src/content/blog/tech-democratization.md`

---

## Issue 006: Configure GitHub Actions Auto-Deployment to GitHub Pages
*   **Status**: `COMPLETED`
*   **Description**: Write a GitHub Actions workflow `.github/workflows/deploy.yml` that triggers on push to the `main` or `master` branch. It should set up Node.js, install dependencies, compile the Astro static files, and deploy them to `gh-pages` or directly through GitHub's custom Pages action.
*   **Deliverables**:
    *   `.github/workflows/deploy.yml`
    *   Astro build target configurations if necessary.
