# MSA Monthly Connect · November 2026

**Build Your Profile: Make Uni Count**, with Jinghan Fu & Zuhair Malik. Built with [Slidev](https://sli.dev).

```bash
npm install
npm run dev      # http://localhost:3030 · presenter view at /presenter
npm run build    # static SPA in dist/
npm run export   # PDF (needs playwright-chromium)
```

## Layout

| Path | Purpose |
| --- | --- |
| `slides.md` | The deck: MSA session setup (welcome, Acknowledgement of Country, captions, host, agenda, programme reminders, survey) around the talk content. Speaker scripts are in each slide's notes. |
| `styles/index.css` | ayu dark palette, Microsoft and MSA brand tokens, typography, and the motion system (`rise`, click reveals, `msa` slide transition, reduced-motion handling). |
| `layouts/` | `cover`, `default`, `center` and `split` (two columns, `::right::` slot). All of them render the `kicker:` frontmatter field above the title. |
| `components/` | `MsLogo`, `MsaLogo`, `Card`, `Person`, `Timeline` (click-driven steps), `QrCode` (generated from a URL), `Browser` (screenshot frame). |
| `slide-bottom.vue`, `global-bottom.vue` | Per-slide footer and the deck progress bar. |

## Conventions

- Colours come from CSS variables only: `--ayu-*` for the palette, `--ms-*` / `--msa-*` for brand colours. Components take a `tone` prop (`blue`, `orange`, `green`, `accent`, `purple`, `teal`, `red`).
- The paragraph straight after a slide's `# Title` is styled as its lede.
- Frontmatter `class: brand` gives a slide the MSA purple surface. Frontmatter `chrome: false` hides the footer and progress bar.
- To update a QR code, change its `url`; the code is generated at runtime.
- The two story timelines (slides 19 → 20) use `transition: view-transition`, so the headshot, title and timeline morph between them.
- Avoid class names that collide with UnoCSS utilities (for example `msa` resolves to `margin-inline-start: auto`, and `filter` and `grid` are utilities too).
