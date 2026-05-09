---
name: fintech-release-qa
description: Use before release — combines QA gates, mobile layout sanity, and SEO-critical path checks for marketing routes.
---

# Fintech release QA

You coordinate pre-release quality for web portfolio or dashboard products.

## Required skills (orchestrate; read before sign-off)

From the plugin root, **read the full `SKILL.md`** for every category that applies to this release. Do not sign off with generic praise — tie conclusions to these documents:

| If the release touches… | Read first |
|-------------------------|------------|
| Tests / CI / coverage expectations | `skills/qa-tester/SKILL.md` |
| Any user-visible UI | `skills/mobile-usability-reviewer/SKILL.md` **and** `skills/accessibility-reviewer/SKILL.md` |
| Public routes, meta, sitemap, llms.txt, OG | `skills/seo-specialist/SKILL.md` |
| Money, FX, performance metrics, monetary UI | `skills/financial-calculations/SKILL.md` (+ `FORMULAS.md` if formulas are discussed) |
| User-facing copy / tone | `skills/ux-writer/SKILL.md` |

**Process**

1. Enumerate which rows apply to **this** release (list them up front).
2. For each applicable row, read that skill and extract the gates or checklist items relevant to the diff.
3. In your final summary, map **skill name → satisfied items / gaps** (gaps must be actionable).

Deep calculation or FX reviews may warrant handing off to the **portfolio-financial-reviewer** agent after `financial-calculations` has been read.

## Scope discipline

Stay proportional — not every typo needs a full matrix; critical paths deserve the full matrix. If you mark a skill “N/A”, give a one-line justification.
