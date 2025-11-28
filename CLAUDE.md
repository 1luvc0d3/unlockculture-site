# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Unlock Culture landing page - a static website for unlockculture.work. This is a single-page HTML site with inline CSS, deployed via GitHub Pages with custom domain configuration through Cloudflare.

**Core Message:** Building intentional organizational cultures through servant leadership and evidence-based transformation.

**Framework:** Process → Predictable Behavior → Habits → Culture

## Deployment Architecture

This site uses GitHub Pages with custom domain configuration:

- **Hosting:** GitHub Pages (static site hosting)
- **DNS:** Cloudflare manages DNS records for unlockculture.work
- **Domain:** Custom domain (unlockculture.work) configured via CNAME file
- **Branch:** Deploys from `main` branch
- **SSL:** HTTPS enforcement enabled through GitHub Pages

**Important Files:**
- `index.html` - Single-page landing site with inline styles
- `CNAME` - Contains custom domain for GitHub Pages
- `README.md` - Setup and deployment instructions

## Development Commands

Since this is a static HTML site, there are no build steps or package managers. To preview locally:

```bash
# Simple HTTP server (Python 3)
python3 -m http.server 8000

# Alternative: Python 2
python -m SimpleHTTPServer 8000

# Alternative: Node.js (if http-server is installed globally)
npx http-server -p 8000
```

Then visit http://localhost:8000

## Deployment Process

Changes pushed to the `main` branch automatically deploy to GitHub Pages. DNS is already configured.

```bash
git add .
git commit -m "Update landing page"
git push origin main
```

Wait a few minutes for GitHub Pages to rebuild (usually 1-3 minutes).

## Architecture Notes

**Single-file Architecture:**
- All HTML, CSS, and content in `index.html`
- No JavaScript dependencies or build process
- Inline styles for simplicity and performance
- Responsive design with mobile breakpoint at 768px

**Design System:**
- Color scheme: Purple gradient (#667eea to #764ba2)
- Typography: System fonts (-apple-system, BlinkMacSystemFont, etc.)
- Layout: Centered card design with gradient background
- Components: Pillars grid (3 cards), framework callout box, CTA button

**Contact:** anbu.ilangovane@unlockculture.work

## Modification Guidelines

When editing this site:
- Keep all styles inline in the `<style>` tag (no external CSS)
- Maintain the existing color scheme and gradient theme
- Test responsive behavior at mobile breakpoint (768px)
- Preserve the framework message: "Process → Predictable Behavior → Habits → Culture"
- Keep the three pillars structure: Discover, Connect, Unlock
