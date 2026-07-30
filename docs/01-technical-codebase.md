# Technical & Codebase SEO

This document outlines the standard operating procedures for auditing a project's technical foundation and codebase for SEO issues.

## 1. HTML Header & Meta Tag Structure
- **H1 Tags**: Every page MUST have exactly one `<h1>`. It must not be empty, dynamically conditionally missing without a fallback, or skipped (e.g., jumping from H1 to H3).
- **Meta Tags**: Ensure unique `title` (50-60 chars) and `meta description` (145-158 chars) on all pages.
- **Canonical URLs**: Verify presence of self-referencing canonical tags, especially for parameterized URLs.
- **Open Graph (OG)**: `og:title`, `og:description`, `og:image`, `og:url` must be present.

## 2. Rendering and Data Fetching
- **Client-Side Rendering (CSR) Anti-Patterns**: SEO-critical content (Titles, descriptions, main article bodies, product details) MUST NOT be loaded exclusively client-side (e.g., via `useEffect` in React or `mounted` in Vue) unless pre-rendered or SSR is active.
- Search engines will miss content hidden behind user interactions (e.g., "Click to show description").
- **Framework Checks**:
  - **Next.js**: Use `next/head`, `getServerSideProps`, `getStaticProps`, or App Router `metadata`.
  - **Vue/Nuxt**: Use `head()` method, `asyncData`.
  - **Django/Rails**: Verify meta tags in base layouts and proper server rendering.

## 3. URL Structure & Routing
- URLs should be clean and descriptive (`/products/running-shoes`), avoiding excessive query parameters for core pages (`/page?id=123`).
- Ensure consistent URL patterns, correct trailing slash handling, and hyphen-separated lowercase words.

## 4. Image SEO Implementation
- Ensure all `<img>` tags have descriptive `alt` attributes. No placeholder text like "image".
- Use descriptive file names (e.g., `red-shoes.jpg` not `IMG_123.jpg`).
- Implement proper lazy loading where applicable.

## 5. Structured Data
- Prefer JSON-LD format over microdata.
- Verify schemas: `Organization`, `Article`, `Product` (requires price/availability/reviews), `FAQPage`, `BreadcrumbList`.
