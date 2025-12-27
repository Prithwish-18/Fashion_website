# Fashion Website (Frontend Only)

A modern, responsive, front-end portfolio/landing site for a fashion brand. Built with plain HTML, CSS and vanilla JavaScript. Features include:

- Responsive CSS grid layout and mobile-first breakpoints
- Splash / fluid visual background using a WebGL fluid canvas
- Animated cursor (dot + lagging outline) and interactive micro‑interactions
- Accessible keyboard support and prefers-reduced-motion handling
- Music toggle control for background audio (optional)
- Smooth section reveal animations and hover effects
- Lightweight — no build-step required (static site)

This repository contains two slightly different HTML/CSS versions (grid_project_2.html and grid_project_2_Version2.html) and stylesheets (grid_2.css / grid_2_Version2.css) so you can pick / iterate on the look you prefer.

---

Table of contents
- Concepts & goals
- Project architecture
- Files & components
- Local setup & configuration
- Accessibility & performance notes
- Contribution guidelines
- License

---

Concepts & goals
- Visual-first portfolio for fashion/creative projects.
- Minimal, typographic-first layout with strong hero/video presence.
- Subtle motion (fluid canvas + heading reveals + micro interactions) to add luxury feel while respecting accessibility preferences.
- No framework lock-in — approachable for designers & front-end devs.

---

Project architecture (high-level)
- Static HTML entry points
  - grid_project_2.html — main version
  - grid_project_2_Version2.html — alternate variant
- CSS
  - grid_2.css — main stylesheet
  - grid_2_Version2.css — alternate stylesheet
- Assets
  - video file(s) (example: pin_man_model.mp4) — place in repository root or update paths
  - audio file(s) for background music (optional)
- JavaScript
  - Inline and small modular scripts inside HTML files:
    - WebGL fluid initialization (via CDN skypack)
    - Smooth cursor (cursor-dot / cursor-outline)
    - Section reveal (IntersectionObserver)
    - Music toggle handler
- Documentation
  - docs/ for architecture, installation, and contribution notes

---

Files & components (what each file does)
- grid_project_2.html
  - Primary HTML page with hero layout, portfolio grid, news, contact form, custom cursor elements, and fluid canvas.
- grid_2.css
  - Core layout, animations, responsive rules, cursor & micro-interaction styles.
- grid_project_2_Version2.html
  - Variant of the main page (differences are mostly cosmetic/asset choices).
- grid_2_Version2.css
  - Variant stylesheet matching the Version2 HTML.
- pin_man_model.mp4 (not included) — recommended location: /assets/videos/pin_man_model.mp4
- your-fashion-track.mp3 or Ishq Jalakar... (not included) — recommended location: /assets/audio/
- docs/*.md
  - ARCHITECTURE.md — deeper description of layout, fluid canvas config and cursor system
  - INSTALLATION.md — step-by-step local run instructions and recommended tools
  - CONTRIBUTING.md — how to contribute, style / commit guidance
  - CHANGELOG.md — place to keep release notes

---

Getting started (quick)
1. Clone the repository:
   git clone https://github.com/Prithwish-18/Fashion_website.git
2. Open the HTML file in a browser:
   - grid_project_2.html
   - or grid_project_2_Version2.html
3. For a nicer local dev experience use a lightweight static server:
   - npm i -g live-server
   - live-server
4. Place required assets:
   - /assets/videos/pin_man_model.mp4
   - /assets/audio/your-fashion-track.mp3
   Update paths in HTML if you put assets elsewhere.

---

Accessibility & performance notes
- Prefers-reduced-motion is respected: the custom cursor and heavy animations are disabled if user preference is set.
- Input fields and contenteditable areas fall back to the native cursor for correct caret behavior.
- Lazy-loading images recommended for production.
- Consider compressing video using H.264 + .webm fallback and serving via a CDN for best performance.
- Provide text alternatives for decorative visuals where appropriate.

---

Deployment
- This is a static front-end site; it can be deployed to GitHub Pages, Netlify, Vercel, or any static host.
- If deploying to GitHub Pages, set the publish branch in repository settings (typically `gh-pages` or `main`).

---

Want me to add these files to the repository?
I can push README.md, .gitignore, LICENSE, and the docs/ files to a branch in your repo. Reply with:
- "Yes, push to main" — or
- "Yes, push to branch: <branch-name>" — or
- "No, show me the files first" (you already have them below).
