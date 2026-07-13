# Adding a new style page

A step-by-step guide (with a checklist) for adding another UI style to the guide so every
page stays consistent. Pages are **self-contained HTML** — no build step.

## Fastest path: copy an existing page

1. Duplicate the page whose layout is closest to what you want, e.g.:
   ```bash
   cp minimalism.html <new-style>.html
   ```
2. Update the content (see the section map below).
3. Add the style to `index.html` (grid card + any counts).
4. Add a row to the table in `README.md` and in `docs/PROJECT-NOTES.md`.
5. Record it in `CHANGELOG.md`.

## Keep these consistent across every page

**Shared `:root` design tokens** — do not diverge from these; they make the guide read as
one document:

```css
:root{
  --bg:#0d1017; --bg2:#141925; --card:#1a2130; --line:#28303f;
  --ink:#eef2f9; --mut:#9aa7bd; --sub:#c3ccdd;
  --acc:#6ea8ff; --acc2:#9d7bff; --good:#3ecf8e; --bad:#ff6b6b; --warn:#ffb454;
  --rad:16px; --mw:1060px;
}
```

The **live demo** inside `.stage` is the one place you deliberately break the shared look
to show the new style's own aesthetic. Everything outside the stage (topbar, hero, section
headers, pros/cons, metrics) stays in the shared style.

## Section map of a style page

| Section | What goes there |
|---------|-----------------|
| `<title>` | `NN. Style Name — UI Style Guide` |
| `.topbar` | Home link + "N / 10" pill (update the total if the count changes) |
| `header.hero` | Number badge, style name (+ optional native-language subtitle), one-line tagline, meta badges |
| `.def` | One-paragraph definition |
| `.stage` | **Live CSS demo** of the style — the centerpiece |
| `.chars` | Characteristic chips (key visual traits) |
| Pros / Cons | Honest, balanced |
| Real-world examples | Named products/sites using the style |
| Metrics (0–5) | maturity, demand, accessibility, effort, support |
| When to use | Short, neutral guidance |
| Outsourcing brief | What to specify to a developer + a11y/perf contract conditions |

## Checklist before committing

- [ ] `<title>` and hero number are correct and sequential
- [ ] Topbar pill total updated everywhere (e.g. `N / 11`) if you changed the count
- [ ] Shared `:root` tokens unchanged; only the demo uses the new aesthetic
- [ ] Live demo renders correctly and is responsive (test narrow widths)
- [ ] Pros & cons are balanced; metrics justified
- [ ] Primary sources linked on the page
- [ ] Card added to `index.html` and it links correctly
- [ ] Row added to `README.md` table and `docs/PROJECT-NOTES.md`
- [ ] Entry added to `CHANGELOG.md`
- [ ] Opens standalone in a browser with no console errors

## Accessibility & performance minimums

Whatever the style, the page should still:

- Maintain readable contrast for body text (WCAG AA where practical).
- Not rely on color alone to convey meaning.
- Respect `prefers-reduced-motion` for any animation.
- Keep the page lightweight — no external requests; inline everything.
