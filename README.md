# Code-Xa — Digital Solutions Website

A modern, SEO-focused, multi-page marketing website for Code-Xa: a digital solutions company in Pakistan. Built with semantic HTML, custom CSS, and vanilla JavaScript. Includes rich SEO metadata, Open Graph/Twitter cards, and JSON-LD schemas.

## Features
- **Multi-page site**: `index.html`, `about.html`, `services.html`, `contact.html`.
- **Strong SEO**: `<meta>` tags, Open Graph, Twitter Cards, `canonical`, `hreflang`, and JSON-LD (`Organization`, `LocalBusiness`).
- **Accessible UI**: Semantic structure, focusable controls, visible CTAs, keyboard-friendly nav.
- **Performance-minded**: Minimal dependencies, optimized structure, responsive layout.
- **Contact form**: Integrated with Web3Forms API.

## Tech Stack
- **Frontend**: HTML5, CSS3, JavaScript (vanilla)
- **UI/UX**: Custom CSS (`style.css`), responsive components
- **Assets**: Favicons, social images (Open Graph/Twitter)
- **3rd-party**: Web3Forms (contact form)

## Project Structure
```
code-xa/
├─ index.html        # Home (Hero, About, Services, FAQ, Contact, Footer)
├─ about.html        # Company story, team, values
├─ services.html     # Detailed services listing
├─ contact.html      # Contact info & form
├─ style.css         # Global styles and components
├─ script.js         # Interactivity (cursor, animations, FAQ toggles, etc.)
├─ favicon.ico, favicon-16x16.png, favicon-32x32.png, apple-touch-icon.png
├─ site.webmanifest
└─ assets/           # (Optional) images, logos, media
```

## Getting Started
### 1) Clone
```bash
git clone https://github.com/Innocent-Developer/code-xa.git
cd code-xa
```

### 2) Run locally
- Option A (VS Code): Install the “Live Server” extension, then “Open with Live Server”.
- Option B (Python):
```bash
# Python 3
python -m http.server 5500
# Visit http://localhost:5500/
```

No build step is required. All files are static and ready to serve.

### 3) Configure the contact form (Web3Forms)
`index.html` contact form uses Web3Forms. Replace the placeholder key with your own:
- File: `index.html`
- Input: `<input type="hidden" name="access_key" value="YOUR-KEY-HERE">`
- Get a free key at: https://web3forms.com/

## Deployment
- **Netlify**
  - New site from Git → connect repo → set publish directory to repository root.
- **GitHub Pages**
  - Settings → Pages → Source: Deploy from branch → select `main` and `/ (root)`.
- **Vercel**
  - Import project → Framework preset: “Other” → output directory: root.

## SEO Checklist (already implemented or recommended)
- **Head tags** in `index.html`:
  - Title, description, keywords, robots
  - Open Graph + Twitter Cards
  - Canonical and hreflang
  - JSON-LD `Organization` and `LocalBusiness`
- **On-page**:
  - Descriptive headings in `#about`, `#services`, `#faq`, `#contact`
  - Internal links: navbar + footer
  - Image `alt` text (ensure all images have meaningful `alt`)
- **Performance**:
  - Compress/optimize hero and social images
  - Prefer modern image formats (WebP/AVIF) where possible
  - Preload critical assets if needed

## Accessibility Checklist
- **Color contrast** meets WCAG AA
- **Keyboard navigation** works for menu and CTAs
- **Landmarks**: use of `<nav>`, `<section>`, headings hierarchy (`h1`→`h2`→`h3`)
- **Focus styles** visible for interactive elements
- **ARIA**: add labels where helpful (e.g., buttons, accordions)

## Scripts and Interactions
- `script.js` powers:
  - Custom cursor and follower
  - Hero typing effect / counters
  - FAQ expand/collapse
  - Back-to-top button

If you add or rename sections in HTML, ensure data attributes/classes referenced in `script.js` are updated accordingly.

## Environment & Secrets
- **Web3Forms access key**: client-side only; do not commit a private server key.
- If you add analytics or other integrations, use environment variables where possible and document them here.

## Contributing
1. Fork the repo
2. Create a feature branch: `git checkout -b feat/your-feature`
3. Commit changes: `git commit -m "feat: add your feature"`
4. Push branch: `git push origin feat/your-feature`
5. Open a Pull Request

## License
Copyright © 2025 Code-Xa. All rights reserved.

If you intend to open-source, replace with your preferred license (MIT/Apache-2.0/etc.).

## Roadmap / Enhancements
- **[SEO]** Dedicated `sitemap.xml` and `robots.txt`
- **[Performance]** Image optimization (WebP/AVIF) and lazy-loading where applicable
- **[Accessibility]** Audit with Lighthouse/axe → fix headings/labels
- **[DX]** Prettier + ESLint configs; simple npm scripts for lint/format
- **[Analytics]** Privacy-friendly analytics (e.g., Plausible)
- **[PWA]** Manifest + Service Worker for offline caching
- **[Testing]** Add basic CI (GitHub Actions) to run link checks and HTML validation

## Contact
- Email: `thecodexaoffical@gmail.com`
- Phone: `+92 316 4392 830`
- Location: Islamabad, Pakistan
- Website: https://code-xa.com
