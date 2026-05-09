# kyberis / cursor-plugins

**Plugin ID:** `trefolio-open-toolkit` (see [`.cursor-plugin/plugin.json`](.cursor-plugin/plugin.json))

Cursor plugin for **portfolio / fintech web apps**: financial calculation discipline, WCAG-oriented UI review, mobile usability, QA patterns, Next.js SEO, and UX writing. Derived from [trefolio (stocktracker)](https://github.com/kyberis/stocktracker); the app does not need to be installed to use this plugin.

**Not investment advice.** Engineering and UX practices only.

**License:** MIT — [LICENSE](LICENSE)

This repository follows the **Open Plugins** layout at the **repo root** ([open-plugins.com](https://open-plugins.com)) so tools like [cursor.directory](https://cursor.directory) can discover `rules/`, `skills/`, and `agents/` without a nested folder.

---

## Layout

| Path | Purpose |
|------|---------|
| [`.cursor-plugin/plugin.json`](.cursor-plugin/plugin.json) | Plugin manifest (name, version, metadata) |
| [`rules/`](rules/) | `.mdc` rules (accessibility trigger, token efficiency, fintech UI, etc.) |
| [`skills/`](skills/) | `*/SKILL.md` — financial-calculations, accessibility-reviewer, mobile-usability-reviewer, qa-tester, seo-specialist, ux-writer |
| [`agents/`](agents/) | Agent personas (`.md`); each agent **binds to** the `skills/` it must read before answering (see each file’s "Required skills" section) |
| [PUBLISH.md](PUBLISH.md) | Cursor Marketplace and directory submission notes |

### Agents and skills

**Agents do not run skills automatically** in the model — they instruct the model to **read** the linked `skills/.../SKILL.md` files first. Open those paths (or use `/skill-name` if your Cursor build exposes skills) so financial, a11y, and QA reviews stay aligned with the packaged skills.

### Included vs omitted (source: internal monorepo)

**Included here** — generalized for open use: financial math patterns, a11y/mobile review flows, QA/SEO/UX guidance without proprietary paths.

**Omitted** — stays in stocktracker [`.cursor/`](https://github.com/kyberis/stocktracker) only: IdP/Stripe/broker-specific skills, device firmware, product-only rules.

---

## Install locally

From the repo root (after `git clone`):

```bash
mkdir -p ~/.cursor/plugins/local
ln -sf "$(pwd)" ~/.cursor/plugins/local/trefolio-open-toolkit
```

Restart Cursor or **Developer: Reload Window**. Remove the symlink when done:

```bash
rm ~/.cursor/plugins/local/trefolio-open-toolkit
```

Docs: [Cursor — Creating plugins](https://cursor.com/docs/plugins).

---

## Publish & list

- **Cursor Marketplace:** submit **this repo URL** at [cursor.com/marketplace/publish](https://cursor.com/marketplace/publish) — see [PUBLISH.md](PUBLISH.md).
- **cursor.directory:** submit the same repo; discovery expects Open Plugins paths at **root** (`rules/*.mdc`, `skills/*/SKILL.md`, `agents/*.md`, …).

---

## trefolio monorepo (submodule)

[Vendored](https://github.com/kyberis/stocktracker) at `cursor-plugins/`:

```bash
git clone --recurse-submodules https://github.com/kyberis/stocktracker.git
# or: git submodule update --init cursor-plugins
```

After editing **this** repo, in stocktracker: `cd cursor-plugins && git pull`, then commit the updated submodule SHA.

---

## Contributing

PRs welcome on **[kyberis/cursor-plugins](https://github.com/kyberis/cursor-plugins)**. Keep content generic; product-specific rules live in stocktracker’s `.cursor/`.
