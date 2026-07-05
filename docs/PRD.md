# Product Requirements Document (PRD)

## Product Name: Byte True Personal Website

A high-performance, minimalist personal website representing **Byte True**, built to showcase their engineering portfolio, host their technical journal, and communicate their core philosophy of **Tech Democratization (科技平权)**.

---

## 1. Overview & Objective

The primary objective is to build a fast, light, and visually striking personal web presence. The design is anchored on a near-black canvas with white uppercase display headlines and sparing M-tricolor accents, signaling engineering precision.

### Core Philosophy
*   **Tech Democratization (科技平权)**: The practice of taking complex, high-ceiling innovations (such as mobile AI agency) and wrapping them in simple, stable, and highly-accessible tools so that anyone can use them.

---

## 2. Technical Stack & Architecture

*   **Framework**: Astro (Static Site Generation - SSG).
*   **Styling**: Tailwind CSS (v4) using `@tailwindcss/vite` integration.
*   **Fonts**: Inter (Google Fonts) as a high-quality display & body font substitute.
*   **Deployment**: GitHub Pages (fully static, auto-deployed via GitHub Actions on push).

---

## 3. Design System (BMW M-Design Inspired)

*   **Canvas**: Pure Black (`#000000`).
*   **Type Contrast**: Intense weight pair — Display headlines in bold UPPERCASE (weight 700, tracked tight `-0.5px`), body text in sentence-case light (weight 300).
*   **Accent Color**: M-Stripe Divider (4px horizontal gradient of Light Blue `#0066b1` → Dark Blue `#1c69d4` → Red `#e22718`).
*   **Border Radius Scale**: Sharp corners (`rounded-none` / `0px`) for all buttons, inputs, and cards. Only circular control elements are circular (`rounded-full`).

---

## 4. Functional Requirements

### 4.1 Global Layout
*   **Header (`top-nav`)**: 64px tall, black canvas background, containing the brand wordmark "BYTE TRUE" with a tricolor indicator on the left, and navigation links (`HOME`, `BLOG`, `GITHUB`) on the right. Active page is highlighted with a bottom underline.
*   **Footer**: Low-contrast black footer displaying the copyright, technical engine indicators, and a summary of the Tech Democratization philosophy.

### 4.2 Home Page (Index)
*   **Hero Photo Band**: High-contrast, dark tech image backdrop with a huge uppercase headline "BYTE TRUE", a subtitle outlining the core philosophy, and an industrial-precision outline CTA button.
*   **Philosophy Section**: A two-column editorial layout explaining "科技平权" (Tech Democratization) in deep, lightweight typography.
*   **Selected Projects Section**: Displays projects from the collection.
    *   **Project Card Layout**: Features a top cover image, an uppercase project title, description, a **`spec-cell` style technical specification grid** (e.g., `METHOD: DOM-BASED`), and a link to the GitHub repository.
*   **Magazine Section**: A 3-up preview of the most recent blog posts, styled as high-contrast bordered cards.

### 4.3 Blog List Page
*   An organized archive of all published articles sorted chronologically by publish date. Cards render as minimal bordered rectangles.

### 4.4 Blog Post Detail Page
*   A clean, single-column article layout optimized for code readability and technical prose.
*   Features custom Markdown styles (without heavy external typography libraries) for headers, lists, code blocks, and blockquotes.

---

## 5. Data & Content Schemas

### 5.1 Blog Post Collection (`blog`)
*   `title` (string): Title of the post (rendered UPPERCASE in lists).
*   `pubDate` (date): Publish date.
*   `description` (string): Short summary for previews.
*   `tags` (array of strings, optional).

### 5.2 Projects Collection (`projects`)
*   `title` (string): Name of the project (rendered UPPERCASE).
*   `description` (string): Project details.
*   `url` (string, optional): External link (GitHub).
*   `techStack` (array of strings, optional).
*   `specs` (record/object of string-to-string key-values, optional): Custom technical specs for `spec-cell` rendering (e.g., `{ "METHOD": "DOM-BASED", "PLATFORM": "ANDROID" }`).
*   `sortOrder` (number, optional): Sort sorting index.
