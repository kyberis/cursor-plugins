# Publishing checklist

## Cursor Marketplace (official)

1. Keep this **public** Git repository as the plugin root (rules/skills/agents at top level—not nested in a subfolder).
2. Update `.cursor-plugin/plugin.json` → `repository` (and optional `homepage`) to match the repo URL.
3. Confirm every rule/skill/agent file has valid YAML frontmatter ([reference](https://cursor.com/docs/reference/plugins)).
4. Test locally via `~/.cursor/plugins/local` (see README).
5. Submit the repo URL at **https://cursor.com/marketplace/publish** and wait for manual review.

## cursor.directory (community)

After the repo is public, you may list it on **https://cursor.directory** for extra discovery (optional; not a substitute for Marketplace submission).

**Layout:** [cursor.directory](https://cursor.directory) expects [Open Plugins](https://open-plugins.com) component paths at the **repository root** (`rules/*.mdc`, `skills/*/SKILL.md`, `agents/*.md`, etc.). This repo is structured that way; do not nest the plugin in a subfolder.

## Team-only distribution

On Cursor **Teams** or **Enterprise**, import a GitHub repo as a **team marketplace** (Dashboard → Settings → Plugins) so plugins stay private to your org.

## After acceptance

- Tag releases with semver aligned with `plugin.json` `version`.
- Document breaking changes in README when rule/skill behavior shifts materially.
