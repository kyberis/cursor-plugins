# Cursor Marketplace plugins

Public repo: **[github.com/kyberis/cursor-plugins](https://github.com/kyberis/cursor-plugins)** — Cursor plugin bundles for the trefolio ecosystem.

| Directory | Description |
|-----------|-------------|
| [`trefolio-open-toolkit/`](trefolio-open-toolkit/) | Rules, skills, and agents for portfolio/fintech web apps ([Marketplace publish](https://cursor.com/marketplace/publish)). |

## trefolio (stocktracker) monorepo

This repository is linked as a **Git submodule** at `cursor-plugins/` inside [kyberis/stocktracker](https://github.com/kyberis/stocktracker). Clone with submodules:

```bash
git clone --recurse-submodules https://github.com/kyberis/stocktracker.git
# or after clone:
git submodule update --init --recursive
```

Day-to-day Cursor rules for core product work remain in the main repo under `.cursor/` (not this submodule).
