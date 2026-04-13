# Project Guidelines

## Build and Test
- Use Node 22+ (recommended through nvm).
- Install dependencies: `npm ci`.
- Local development: `npm run dev`.
- Production build: `npm run build`.
- Verify static output locally: `npm run preview`.

## Architecture
- This repository is an Astro static website deployed to GitHub Pages.
- Keep the scope homepage-first until explicit request to migrate additional pages.
- Main page entry point is `src/pages/index.astro`.
- Shared HTML metadata and base document belong in `src/layouts/MainLayout.astro`.

## Conventions
- Keep content in Polish unless user asks for multilingual output.
- Prefer semantic HTML sections and clear heading hierarchy.
- Do not add client-side frameworks unless there is a measurable need.
- Keep dependencies minimal and focused on static-site generation.

## Images
- Place original raster images in `src/assets/images/`.
- Use Astro `Picture`/`Image` from `astro:assets` for optimized output.
- Default to responsive widths and modern formats (`avif`, `webp`) with meaningful alt text.
- Do not place large content images in `public/` because this bypasses optimization.

## Deployment
- GitHub Actions deploy workflow lives in `.github/workflows/deploy.yml`.
- Production domain is `ma-elektro.pl` via GitHub Pages custom domain.
- Keep `public/CNAME` aligned with the current domain.
