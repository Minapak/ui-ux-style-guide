# Project Notes — "Memory" for this repo

> This file is the living memory of the project. Read it first before making changes,
> and update it whenever you add a style, change a decision, or learn something worth
> keeping. Keep it factual and dated.

## What this is

A neutral, at-a-glance reference to common **UI design styles**, built to share with
clients who don't yet have a UI/UX guide. Each style has its own self-contained HTML page
with a **live CSS demo** (not a screenshot), honest pros & cons, real-world examples,
neutral 0–5 metrics, and an outsourcing brief.

- **Audience:** clients, PMs, and developers evaluating a look-and-feel direction.
- **Tone:** neutral. No style is "best" — the right choice depends on the project.
- **Tech:** self-contained HTML with inline CSS/JS. No build step, no dependencies.

## Current contents (as of 2026-07-13)

10 style pages, linked from `index.html`:

| # | Style | File |
|---|-------|------|
| 01 | Skeuomorphism | `skeuomorphism.html` |
| 02 | Neumorphism | `neumorphism.html` |
| 03 | Glassmorphism | `glassmorphism.html` |
| 04 | Claymorphism | `claymorphism.html` |
| 05 | Minimalism | `minimalism.html` |
| 06 | Maximalism | `maximalism.html` |
| 07 | Brutalism | `brutalism.html` |
| 08 | Liquid Glass | `liquid-glass.html` |
| 09 | Bento Grid | `bento-grid.html` |
| 10 | Spatial UI | `spatial-ui.html` |

Supporting files: `index.html` (landing + full grid), `README.md`, `LICENSE` (MIT),
`.nojekyll` (so GitHub Pages serves files as-is).

## Design decisions (why things are the way they are)

- **Dark theme, shared token set.** Every page reuses the same CSS custom properties in
  `:root` (`--bg`, `--card`, `--ink`, `--acc`, `--rad`, etc.). Keep these consistent
  across pages so the guide reads as one document. See `docs/ADDING-A-STYLE.md` for the
  token list.
- **Live demos, not images.** Each "stage" renders the style with real CSS. This is the
  whole point — it shows the style behaving, and stays crisp on any screen.
- **Neutral 0–5 metrics.** maturity, demand, accessibility, effort, support. They're
  relative references, kept as objective as possible. If you revise one, note the reason
  in the CHANGELOG.
- **Self-contained pages.** No shared stylesheet or JS bundle on purpose — each page opens
  standalone. The cost is duplicated CSS; the benefit is zero build and easy sharing.

## Roadmap / ideas for later

- [ ] Candidate styles to add: Flat Design, Material 3 / Material You, Swiss / International
      Typographic, Y2K / Frutiger Aero, Dark Mode patterns, Retro / Pixel, Memphis.
- [ ] Optional: a shared print/PDF export for handing the whole guide to a client offline.
- [ ] Optional: light-theme toggle.
- [ ] Optional: per-style "starter CSS" download button.

## How to work on this repo

- Adding a new style → follow `docs/ADDING-A-STYLE.md` (has a checklist).
- Record every user-visible change in `CHANGELOG.md`.
- Deploying → see the GitHub Pages section in `README.md`.

## Sources & credibility

Factual claims cite primary sources per page (Apple HIG, Nielsen Norman Group, Interaction
Design Foundation, and others). When adding claims, prefer primary sources and link them on
the page itself so clients can verify.

## Change log of this notes file

- **2026-07-13** — Initial project notes created; 10 styles catalogued; repo published to
  GitHub under `Minapak`.
