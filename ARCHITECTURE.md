# Architecture & Design Notes

This document explains the architecture and design decisions for the Fashion_website front-end.

Core concepts
- Single-page static structure: content arranged in vertically stacked sections (home, portfolio, fashion-week, news, contact).
- Left-heavy hero: the main grid places typographic content on the left and a video on the right for visual depth.
- Visual layering:
  - WebGL fluid canvas (`#fluid`) sits fixed and uses multiply blending to produce drifting color/smoke behind content.
  - Heading reveal animations are CSS-only using keyframes + staggered delays for an elegant sequence.
- Micro interactions:
  - Cursor system: a fast-moving dot plus a lagging outline; hover states enlarge and color the cursor to match brand accent (orangered).
  - Music toggle: three-bar visual battery that animates when audio plays and toggles aria-pressed for accessibility.
- Progressive enhancement:
  - If JS disabled: all content remains usable; cursor elements hidden via <noscript>.
  - If WebGL not available: fluid canvas will fail gracefully — the site remains fully usable.

Modules / responsibilities
- HTML pages:
  - Present semantic structure and interactive hooks (.cursor-dot, .cursor-outline, #music-toggle, #fluid).
- CSS:
  - Layout and responsive behavior (CSS Grid + flexbox).
  - Animations (keyframes for fadeInUp, scaleIn).
  - Cursor & micro-interaction styling and reduced-motion support.
- Inline JS (per HTML file):
  - Initialize WebGLFluid (3rd-party module from skypack CDN).
  - Implement custom cursor logic (pointermove listeners + requestAnimationFrame to animate outline).
  - IntersectionObserver for reveal-on-scroll.
  - Music toggle control with keyboard support and aria updates.

WebGLFluid configuration (recommended defaults in HTML)
- SIM_RESOLUTION: 128
- DYE_RESOLUTION: 1024 (higher for smoother "silk")
- DENSITY_DISSIPATION: 2.5
- VELOCITY_DISSIPATION: 1.5
- PRESSURE: 0.8
- CURL: ~10 for subtle swirls
- SPLAT_RADIUS: ~0.2
- SHADING: true, TRANSPARENT: true
- onSplat: use brand palette (gold, orangered, smoked black)

Accessibility considerations
- `prefers-reduced-motion: reduce` turns off custom cursor & heavy animations
- Interactive areas are keyboard-focusable, and the cursor hover is mirrored on focus for keyboard users
- Form input fields use native caret (custom cursor hidden)

Performance tips
- Compress and provide multiple formats for video (webm + mp4)
- Optimize images and use srcset for responsive images
- Consider reducing DYE_RESOLUTION on low-end devices
- Bundle and cache third-party resources where possible for production
