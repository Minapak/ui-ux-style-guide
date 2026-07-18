# UI Design Styles — A Quick Reference Guide

A neutral, at-a-glance reference to **11 common UI design styles**, built to share with
clients who don't yet have a UI/UX guide. Each style page includes a **live demo rendered
with real CSS** (not a screenshot), honest **pros & cons**, real-world examples, neutral
0–5 metrics, and a short note on when to use it.

> Curated as of **July 2026** with current, credible sources (Apple, Nielsen Norman Group,
> Interaction Design Foundation, and others). Presented neutrally — no style is "best";
> the right choice depends on the project.

## 🔗 Live site

Once GitHub Pages is enabled (see below), the guide is served at:

```
https://minapak.github.io/ui-ux-style-guide/
```

Open `index.html` to start.

## 🎨 The styles

| # | Style | One-line summary |
|---|-------|------------------|
| 01 | [Skeuomorphism](skeuomorphism.html) | Imitates real-world objects — textures and 3D buttons that feel touchable. |
| 02 | [Neumorphism](neumorphism.html) | Soft UI where elements extrude from a same-color background via dual shadows. |
| 03 | [Glassmorphism](glassmorphism.html) | Frosted-glass panels blurring the background — depth and polish at once. |
| 04 | [Claymorphism](claymorphism.html) | Puffy soft-clay 3D shapes with inner + outer shadows. |
| 05 | [Minimalism](minimalism.html) | Whitespace, restrained color and typography — the most durable approach. |
| 06 | [Maximalism](maximalism.html) | Bold color, huge type and overlap — planned abundance, minimalism's opposite. |
| 07 | [Brutalism](brutalism.html) | Raw, unpolished web — default fonts, harsh borders, stark contrast. |
| 08 | [Liquid Glass](liquid-glass.html) | Apple's 2025 material — reflects/refracts like glass while flowing like liquid. |
| 09 | [Bento Grid](bento-grid.html) | Modular grid of differently-sized cells, like a Japanese bento box. |
| 10 | [Spatial UI](spatial-ui.html) | Interface placed in 3D depth — the language of spatial computing (visionOS). |
| 11 | [Flat Design](flat-design.html) | No shadows, gradients or textures — bold solid color and simple shapes. The reaction to skeuomorphism. |

Each page also carries an **outsourcing brief**: what to specify to a developer and which
accessibility / performance conditions to put in the contract.

## 🚀 Publish to GitHub Pages

1. Create a new **public** repository on GitHub.
2. Add these files and push:
   ```bash
   git init
   git add .
   git commit -m "UI design styles reference guide"
   git branch -M main
   git remote add origin https://github.com/Minapak/ui-ux-style-guide.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages**, set **Source** to `Deploy from a branch`,
   pick `main` / `/ (root)`, and save.
4. Wait ~1 minute — your guide is live at the URL above.

`.nojekyll` is included so GitHub Pages serves the files as-is.

## 🧩 Extending this guide

This repo is set up to grow over time. Relevant docs:

- [`docs/PROJECT-NOTES.md`](docs/PROJECT-NOTES.md) — project "memory": context, design
  decisions, roadmap, and sources. **Read this first** before making changes.
- [`docs/ADDING-A-STYLE.md`](docs/ADDING-A-STYLE.md) — step-by-step guide + checklist for
  adding a new style page while keeping everything consistent.
- [`CONTRIBUTING.md`](CONTRIBUTING.md) — ground rules and workflow.
- [`CHANGELOG.md`](CHANGELOG.md) — record of every user-visible change.

## 📎 Notes

- Everything is **self-contained HTML** (inline CSS/JS, no build step, no dependencies).
  Every page works by simply opening the file in a browser.
- The demos are illustrative CSS implementations of each style, not production components.
- Metrics (maturity, demand, accessibility, effort, support) are relative references as of
  July 13, 2026, kept as objective as possible.

## 📄 License

Code and markup: [MIT](LICENSE). The descriptive text is provided as a neutral reference;
please cite the linked primary sources (listed on each page) when reusing factual claims.
