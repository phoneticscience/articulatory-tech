# Session Log: 2026-02-22

## What was done

### Project Setup
- Scaffolded Astro project with minimal template
- Installed Tailwind CSS v4 via `@tailwindcss/vite` integration
- Configured brand colors in `src/styles/global.css` using Tailwind v4 `@theme`:
  - Navy: `#1B2A4A` (primary brand color)
  - Blue: `#4A7ABF` (accent/CTA)
  - Green: `#5A8A5A` (secondary accent)
- Set Inter as the primary font family
- Configured `astro.config.mjs` with site URL `https://articulatory.tech`

### Landing Page Components
- **BaseLayout.astro**: HTML shell with meta tags, OG tags, Google Fonts, favicon
- **Header.astro**: Sticky nav bar with logo wordmark, nav links (News, Solutions, About), mobile hamburger menu, responsive at `sm:` breakpoint
- **Hero.astro**: Centered logo, brand heading, tagline "Articulatory measurement. Visualization. Software."
- **News.astro**: News section with left-border card layout. First entry: Speech Prosody 2026 Show and Tell (placeholder details)
- **Mission.astro**: "Focus Areas" section with 3 cards + inline SVG icons (waveform, graph, code brackets). Technical-direct copy style.
- **About.astro**: Founder bio — Jaekoo Kang, PhD (Speech Science, CUNY Graduate Center)
- **Footer.astro**: Navy background, copyright, jaekookang.me link

### Quality Improvements
- Replaced emoji icons with inline SVG line-art icons
- Rewrote all copy to remove AI-sounding phrasing and "We" subject
- Added 3-tier responsive breakpoints (phone / tablet / desktop)

### Deployment
- Created `.github/workflows/deploy.yml` for GitHub Actions -> GitHub Pages
- Created `.gitignore`

### Verification
- `npm run build` succeeds, output in `dist/`

## File Structure
```
src/
  layouts/BaseLayout.astro
  components/Header.astro, Hero.astro, News.astro, Mission.astro, About.astro, Footer.astro
  pages/index.astro
  styles/global.css
public/images/logo.png
.github/workflows/deploy.yml
astro.config.mjs
```

## TODOs
- [x] Scaffold Astro + Tailwind project
- [x] Build landing page components
- [x] Remove emojis, rewrite copy, improve responsive design
- [x] Add News section (Speech Prosody 2026)
- [x] Initialize git repo and push to GitHub
- [x] Configure GitHub Pages: enable Pages, set source to GitHub Actions
- [x] Configure custom domain `articulatory.tech` in GitHub Pages settings
- [x] Verify CloudFlare DNS CNAME -> GitHub Pages
- [ ] Fill in Speech Prosody 2026 details (date, location, title)
- [ ] Create favicon (cropped/simplified logo at 32x32)
- [ ] Add Blog section
- [ ] Add contact/email section
- [ ] Add Disqus or similar for blog comments
