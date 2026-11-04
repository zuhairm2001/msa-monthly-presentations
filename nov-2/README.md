# MSA Monthly Connect · November 2026 · Alternative deck

**Software Engineering: From Design to Oncall**, with Jinghan Fu & Zuhair Malik. A standalone [Slidev](https://sli.dev) presentation; the original `../nov` deck is unchanged.

```bash
cd nov-2        # from the repository root
npm ci
npm run dev    # http://localhost:3030 · presenter view at /presenter
npm run build  # static SPA in dist/
npm run export # PDF (needs playwright-chromium and its browser)
```

## Session

45 minutes including welcome, discussion and feedback. Speaker notes assign each slide to Jinghan, Zuhair or both and include suggested timing.

| Topic | Focus |
| --- | --- |
| Day in the life, with AI | A representative day, faster feedback loops, human accountability and safe AI use |
| Design reviews | Requirements, alternatives, trade-offs, failure modes and a decision record |
| Implementation | Small changes, tests, code review, staged rollout and rollback |
| Oncall | Triage, mitigation, communication, escalation and learning |
| Alerting and monitoring | Metrics, logs, traces, SLIs/SLOs and actionable alerts |
| AKS scale | Pods, nodes, clusters, fleets, autoscaling and capacity bottlenecks |

The talk follows a **fictional job-processing service**. Its latency targets, alert settings, capacity figures and incident are teaching examples, not claims about the presenters' work or Microsoft's production infrastructure. AKS capacity arithmetic is explicitly illustrative, not a supported-limit statement; the final resources slide links to official documentation for current limits and guidance.

## Structure and styling

- `slides.md`: all slides and presenter notes, including welcome, Acknowledgement of Country, captions, presenters, Q&A and the existing feedback link.
- `styles/index.css`: the original ayu dark / MSA palette and motion system, plus the alternative deck's reusable content grids.
- `layouts/`, `components/`, `public/`: copied from `nov` so this alternative can run and deploy independently.
- `slide-bottom.vue`, `global-bottom.vue`: slide footer and progress indicator.

Use the existing `Card`, `Person`, `QrCode` and `Browser` components, `kicker:` frontmatter, and CSS colour variables. `layout: split` uses the `::right::` slot. Use `v-click` for progressive reveals; speaker notes explain the talking points.
