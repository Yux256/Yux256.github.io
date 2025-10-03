# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Essential Development Commands

### Package Management & Development Server
- `pnpm install` - Install all dependencies (Tailwind CSS v4, Preact, etc.)
- `pnpm run dev` - Start Hugo development server with `--disableFastRender`
- `pnpm run build` - Build site with `hugo --minify` for production

### Advanced Hugo Commands
For direct Hugo usage beyond package.json scripts:
- `hugo server --disableFastRender` - Development server (equivalent to `pnpm run dev`)
- `hugo --gc --minify` - Production build with garbage collection
- `hugo --buildFuture` - Include future-dated content
- `hugo version` - Check Hugo version (should be 0.150.1 Extended)

### Search Index Generation
- `pnpm dlx pagefind --source 'public'` - Generate search index after building

## Architecture Overview

This is a **Hugo Blox Builder** academic CV site using:

- **Hugo Static Site Generator** (v0.150.1 Extended required)
- **Hugo Blox Builder Framework** - Block-based page composition system
- **Tailwind CSS v4** - Utility-first CSS framework 
- **Go Modules** - Theme and plugin management via `go.mod`
- **pnpm** (v10.14.0) - Package manager for Node.js dependencies

### Block-Based Landing Page System
The homepage (`content/_index.md`) uses a declarative block system where each section is defined as a block type (e.g., `resume-biography-3`, `collection`, `markdown`). Blocks can be reordered, configured, and styled independently.

### Content Architecture
- **Authors** (`content/authors/admin/`) - Rich author profiles with education, work history, skills
- **Publications** (`content/publications/`) - Academic papers with BibTeX metadata, DOIs, links
- **Projects** (`content/projects/`) - Research and development projects
- **Blog** (`content/blog/`) - News and article content
- **Events** (`content/events/`) - Talks, conferences, presentations

## Key Development Workflows

### Publication Management
- **Auto-import from BibTeX**: Place `publications.bib` in root → GitHub Actions automatically converts to Markdown pages via `academic` Python package
- **Manual creation**: Create folders in `content/publications/` with `index.md` files using publication front matter schema

### Deployment Pipeline
- **GitHub Pages**: Automatic deployment on push to `main` branch via `.github/workflows/deploy.yml`
- **Netlify**: Alternative deployment configured in `netlify.toml` with advanced build settings
- Build process: `pnpm install` → `hugo --minify` → `pagefind` indexing

### Version Requirements
- Hugo: 0.150.1 Extended (specified in `hugoblox.yaml` and workflows)
- Go: 1.19+ (for Hugo modules)
- Node.js: 20+ (for Tailwind CSS and build tools)
- pnpm: 10.14.0 (package manager)

## Important File Structure

### Configuration
- `hugoblox.yaml` - Hugo Blox Builder template configuration
- `config/_default/hugo.yaml` - Main Hugo site configuration
- `go.mod` - Hugo modules for theme management
- `package.json` - Node.js dependencies and build scripts

### Content Management
- `content/_index.md` - Landing page with block-based sections
- `content/authors/admin/_index.md` - Primary author profile (superuser)
- `content/publications/` - Academic publications with rich metadata
- `content/blog/`, `content/projects/`, `content/events/` - Additional content types

### Build & Deployment
- `.github/workflows/deploy.yml` - GitHub Pages deployment
- `.github/workflows/import-publications.yml` - BibTeX auto-import
- `netlify.toml` - Netlify deployment configuration
- `layouts/partials/` - Custom Hugo template overrides

## Content Management Guidelines

### Publication Metadata Standards
- Include `doi` in `hugoblox.ids` for auto-linking
- Use `featured: true` to highlight key publications
- Provide multiple link types: `pdf`, `code`, `dataset`, `slides`, `video`
- Set `publication_types` using CSL standard values
- Add `abstract` and shorter `summary` for different contexts

### Author Profiles
- Configure rich profiles with education timeline, work history, skills, interests
- Use `superuser: true` for primary site author
- Include social profiles with proper icon references
- Add awards, languages, and custom skill categories

### Content Organization
- Use folder-based content organization (Hugo page bundles)
- Include `featured.jpg/png` images for visual content
- Leverage front matter for metadata-driven page generation
- Cross-reference content via folder names and taxonomies