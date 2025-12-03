# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Build and Development Commands

```bash
npm run dev       # Start local dev server at localhost:4321
npm run build     # Build production site to ./dist/
npm run preview   # Preview production build locally
npm run astro     # Run Astro CLI commands (e.g., `npm run astro add`)
```

## Architecture

This is an Astro 5.x portfolio site using file-based routing and content collections.

**Key directories:**
- `src/pages/` - File-based routing (index.astro, about.astro, work.astro, work/[...slug].astro for dynamic routes)
- `src/content/work/` - Markdown files for portfolio items, validated by Zod schema in `src/content.config.ts`
- `src/components/` - Astro components including custom elements (ThemeToggle, Nav menu button)
- `src/layouts/BaseLayout.astro` - Main page layout wrapper
- `src/styles/global.css` - CSS custom properties for theming (gray scale, accent colors, breakpoints at 50em/60em)
- `public/assets/` - Static images including responsive backgrounds for light/dark themes

**Content Collection Schema** (`src/content.config.ts`):
- Required: title, description, publishDate, tags (array), img
- Optional: img_alt

**Theme System:** CSS variables with light/dark mode toggle. Theme preference persisted to localStorage.
