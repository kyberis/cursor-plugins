# kyberis / cursor-plugins

Cursor **plugin bundles** derived from the [trefolio](https://github.com/kyberis/stocktracker) stack—rules, skills, and agents you can install locally or submit to the [Cursor Marketplace](https://cursor.com/marketplace).

**License:** MIT · **Upstream app:** [stocktracker](https://github.com/kyberis/stocktracker) (not required to use these plugins)

---

## Plugins in this repository

| Plugin | Folder | What it’s for |
|--------|--------|----------------|
| **trefolio-open-toolkit** | [`trefolio-open-toolkit/`](trefolio-open-toolkit/) | Portfolio / fintech web apps: financial calculation discipline, WCAG-oriented UI review, mobile usability, QA patterns, Next.js SEO, UX writing. See its [README](trefolio-open-toolkit/README.md). |

Manifest (Cursor plugin format): [`trefolio-open-toolkit/.cursor-plugin/plugin.json`](trefolio-open-toolkit/.cursor-plugin/plugin.json).

**Disclaimer:** educational tooling only—not investment, tax, or legal advice.

---

## Install locally (try before Marketplace)

From a clone of **this** repo:

```bash
cd trefolio-open-toolkit
mkdir -p ~/.cursor/plugins/local
ln -sf "$(pwd)" ~/.cursor/plugins/local/trefolio-open-toolkit
```

Restart Cursor or run **Developer: Reload Window**. Remove the symlink when you’re done iterating.

Official layout reference: [Cursor — Creating plugins](https://cursor.com/docs/plugins).

---

## Publish on Cursor Marketplace

1. Ensure [`plugin.json`](trefolio-open-toolkit/.cursor-plugin/plugin.json) metadata is accurate (`repository` points here).
2. Follow the checklist in [`trefolio-open-toolkit/PUBLISH.md`](trefolio-open-toolkit/PUBLISH.md).
3. Submit **this repository URL** at [cursor.com/marketplace/publish](https://cursor.com/marketplace/publish) (not the whole stocktracker monorepo).

Optional discovery: [cursor.directory](https://cursor.directory).

---

## Relation to the trefolio monorepo

This repo is vendored into [kyberis/stocktracker](https://github.com/kyberis/stocktracker) as a **Git submodule** at `cursor-plugins/` so product work stays in `.cursor/` while this tree stays small and Marketplace-friendly.

```bash
git clone --recurse-submodules https://github.com/kyberis/stocktracker.git
# or after a plain clone:
git submodule update --init cursor-plugins
```

To bump the submodule pointer after changing **this** repo: in stocktracker, `cd cursor-plugins && git pull`, then commit the updated submodule SHA on `main`.

---

## Contributing

Issues and PRs welcome against **[kyberis/cursor-plugins](https://github.com/kyberis/cursor-plugins)**. Keep plugins generic (no proprietary URLs or internal runbooks); product-specific rules stay in stocktracker’s `.cursor/` directory.
