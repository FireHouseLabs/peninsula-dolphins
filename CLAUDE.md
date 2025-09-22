# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

All commands are run from the root of the project:

| Command | Action |
|---------|--------|
| `npm install` | Install dependencies |
| `npm run dev` | Start local dev server at `localhost:4321` |
| `npm run build` | Build production site to `./dist/` |
| `npm run preview` | Preview build locally before deploying |
| `npm run astro ...` | Run CLI commands like `astro add`, `astro check` |

## Architecture

This is an Astro 5.x project using the "basics" starter template with TypeScript support.

### Project Structure
```
src/
├── components/        # Reusable Astro components
│   └── Welcome.astro  # Main welcome component with styling
├── layouts/          # Page layouts
│   └── Layout.astro  # Base HTML layout with global styles
├── pages/            # File-based routing
│   └── index.astro   # Homepage
└── assets/           # Static assets (SVGs, images)
```

### Key Technologies
- **Astro 5.x**: Static site generator with component islands
- **TypeScript**: Strict configuration (`astro/tsconfigs/strict`)
- **ESM**: Project uses ES modules (`"type": "module"` in package.json)

### Component Patterns
- Astro components use frontmatter (between `---`) for logic/imports
- Styles are scoped by default using `<style>` blocks
- Assets are imported as modules and accessed via `.src` property
- Layout components use `<slot />` for content injection

### Build Output
- Development: Runs on `localhost:4321`
- Production: Builds to `./dist/` directory
- Static assets are optimized and bundled automatically