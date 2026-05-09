# trefolio-open-toolkit

Cursor plugin: rules, skills, and agents for building **portfolio / fintech web apps** — financial calculation discipline, WCAG-oriented reviews, mobile usability, QA patterns, Next.js SEO, and UX writing.

**Not investment advice.** This package encodes engineering and UX practices only.

## Repository layout

This toolkit lives in the standalone repo **[github.com/kyberis/cursor-plugins](https://github.com/kyberis/cursor-plugins)** at `trefolio-open-toolkit/`. The manifest is [`.cursor-plugin/plugin.json`](.cursor-plugin/plugin.json).

In the **trefolio** monorepo ([stocktracker](https://github.com/kyberis/stocktracker)), that repo is attached as a **submodule** at `cursor-plugins/` (so this path is `cursor-plugins/trefolio-open-toolkit/` after clone with `--recurse-submodules`).

Submit the **[cursor-plugins](https://github.com/kyberis/cursor-plugins)** repository URL to the [Cursor Marketplace](https://cursor.com/marketplace/publish) (not the whole stocktracker monorepo).

## Contents

| Component | Purpose |
|-----------|---------|
| `rules/` | Triggers and guardrails (accessibility trigger, token efficiency, fintech UI disclaimers, design tokens reference) |
| `skills/` | `financial-calculations`, `accessibility-reviewer`, `mobile-usability-reviewer`, `qa-tester`, `seo-specialist`, `ux-writer` |
| `agents/` | Short personas that delegate to skills |

### Included vs intentionally omitted

**Included** — generalized from internal practices for open distribution:

- Financial math discipline + formula reference (generic)
- Accessibility and mobile usability review workflows
- QA, SEO, UX writing patterns without proprietary paths

**Omitted** — remains in the private monorepo `.cursor/` only:

- Product-specific integrations (IdP, Stripe internals, broker parsers, hardware, social graph)
- Rules tied to one deployment (`landing-page`, `demo-page`, internal cron registry, etc.)

## Local testing

```bash
mkdir -p ~/.cursor/plugins/local
ln -sf "$(pwd)" ~/.cursor/plugins/local/trefolio-open-toolkit
# Restart Cursor or: Developer: Reload Window
```

Remove the symlink when finished iterating:

```bash
rm ~/.cursor/plugins/local/trefolio-open-toolkit
```

## Publish

See [PUBLISH.md](PUBLISH.md).

## License

MIT — see [LICENSE](LICENSE).
