# Contributing

This is a personal reference project, but it's structured so it can grow cleanly over time.

## Quick start

- **Add a new style page** → follow [`docs/ADDING-A-STYLE.md`](docs/ADDING-A-STYLE.md).
- **Understand the project & decisions** → read [`docs/PROJECT-NOTES.md`](docs/PROJECT-NOTES.md).
- **Record every user-visible change** → update [`CHANGELOG.md`](CHANGELOG.md).

## Ground rules

1. **Stay neutral.** No style is "best"; describe trade-offs honestly.
2. **Keep pages self-contained.** Inline CSS/JS, no external requests, no build step.
3. **Reuse the shared design tokens** (see the adding-a-style guide) so the guide reads as
   one document. The live demo is the only place to express the new style's aesthetic.
4. **Cite primary sources** on the page for any factual claim.
5. **Test standalone** — every page must open correctly by just double-clicking the file.

## Workflow

```bash
# edit or add files, then:
git add .
git commit -m "Add <style>: <short note>"
git push
```

GitHub Pages (if enabled) redeploys automatically from `main`.
