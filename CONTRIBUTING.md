# Contributing

Thanks for contributing! The project is intentionally small and framework-free to make it easy for designers and devs to jump in.

How to contribute
1. Fork the repository
2. Create a feature branch
   git checkout -b feature/short-description
3. Make small, focused commits. Use clear commit messages:
   - feat: add music toggle
   - fix: cursor hide on input focus
   - chore: update README
4. Open a pull request to the main repository and describe your changes.

Code style and guidelines
- HTML: semantic tags where applicable; avoid inline styles except for quick prototypes
- CSS: prefer variables for repeated values (colors, spacing) — keep files organized
- JS: minimal, readable vanilla JS. Prefer small helper functions and avoid global pollution

Accessibility & testing
- Add keyboard support for any interactive element
- Respect prefers-reduced-motion
- Test on desktop & mobile; verify performance of the fluid canvas

Issue reporting
- Use issues to file bugs or enhancement requests. Include:
  - Steps to reproduce
  - Browser & OS
  - Replication URL or code snippet

License & Code of Conduct
- See LICENSE
- Be respectful in reviews and issues
