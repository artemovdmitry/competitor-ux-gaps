# Competitor UX Gaps (SEO platforms, 2026)

> Hands-on UX teardown of five SEO platforms — Semrush, SE Ranking, AgencyAnalytics, Ahrefs, SEOWORK — with twelve concrete UX gaps the next platform should fill. Notes from research before building [Handoff](https://handoff-smooth-transitions.lovable.app/).

This is a working analyst's notebook, not a vendor comparison. It exists because before building the Handoff product I needed an honest read on what the existing toolset actually does, where it shines, and — more importantly — where there are *structural* gaps that no incumbent has incentive to close.

The headline finding: every existing platform is structured around the assumption that **the agency, not the brand, owns the workspace**. None of the five has a handover protocol, an escrow concept, or a marketplace of vetted SEO contractors. These are not oversights; they are emergent consequences of the agency-led business model. They are also the gaps where Handoff differentiates.

## Files

- [`feature-matrix.md`](./feature-matrix.md) — 30+ features × 5 platforms, with ✅ / ◐ / ✗ ratings
- [`platform-deep-dives.md`](./platform-deep-dives.md) — what I saw in trial accounts of each platform
- [`twelve-gaps.md`](./twelve-gaps.md) — the twelve UX gaps, ranked, with how Handoff addresses each
- [`top-10-ideas-to-borrow.md`](./top-10-ideas-to-borrow.md) — the strongest UX patterns the existing platforms got right

## TL;DR

Five all-in-one SEO platforms, ranked by how broadly they cover the SEO PM surface:

| Platform | Strongest feature | Weakest feature | Pricing entry |
|---|---|---|---|
| **Semrush** | App Center extensibility (61+ tools) | Project lifecycle (Agency Growth Kit was sunset) | $140/mo |
| **SE Ranking** | Marketing Plan + task → tool deep-linking | Multi-client agency view (basic) | $65/mo |
| **AgencyAnalytics** | Widget-builder + 80 native integrations + "Ask AI" | No native SEO data layer | $79/mo |
| **Ahrefs** | Site Audit prioritisation + Brand Radar (AI-search) | No PM/task surface at all | $129/mo |
| **SEOWORK** | Plan/Fact tracking with per-employee productivity score | Limited outside the RU/CIS region | ≈$120/mo |

What none of them have:

1. Handover protocol (export/import a portable bundle between platforms)
2. Asset escrow concept (`TRANSFERRED` / `ESCROW` / `PENDING` lifecycle on credentials, links, briefs)
3. Project ownership = client model (the project lives with the brand; the agency is invited)
4. Marketplace of vetted SEO contractors (Stripe Connect–style payouts, in-product workflow)
5. Modular roadmap-builder from typed task-blocks (drag-drop, SEO-aware Linear)
6. Outcome-tracking on tasks (expected outcome → measured actual outcome → contractor productivity score)
7. SEO-team specific roles (PM, Tech SEO, Link-builder, Outreach, Content) instead of generic ones
8. ASO integration (App Store + Google Play + Huawei) alongside SERP/Local/AI-search
9. Cross-channel KPI aggregation (SERP + ASO + Local + AI in one dashboard)
10. Switch-agency wizard (3-step automated transition flow)
11. Audit-trail for legal-grade handover
12. Free public "Reality Check" tool that audits the brand's current agency

The full case for each gap is in [`twelve-gaps.md`](./twelve-gaps.md).

## Method

Direct hands-on access to working accounts of all five platforms, navigation of the full sidebar of each, screenshots and field-level notes. Cross-referenced against vendor documentation, recent product changelogs, and the previous UI analysis from earlier in the project.

The five platforms were chosen to span:

- The two SEO-data leaders (Semrush, Ahrefs)
- The closest PM/agency competitor (SE Ranking)
- The reporting/dashboard leader (AgencyAnalytics)
- A regional reference for in-house/agency PM philosophy (SEOWORK, RU/CIS)

What I did not analyse here: BrightEdge, Conductor, Botify, Lumar (enterprise tier — different ICP), MarketMuse, Surfer (content-led — adjacent), or the niche AI-search tools (Profound, Peec, Otterly).

## What I'm doing with this

Building [Handoff](https://handoff-smooth-transitions.lovable.app/) — focused on the twelve gaps above, with the handover protocol as the wedge. The full prioritised feature list and 36-month roadmap are in the parent project; this repo is the public competitive baseline.

## Author

[Dmitry Artemov](https://www.linkedin.com/in/dmitry-artemov-62384163/) — 16 years in SEO across LG Russia, Zvuk/Sber, and a small agency I closed to build Handoff.
