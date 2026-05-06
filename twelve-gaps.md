# Twelve UX gaps in existing SEO platforms

The twelve gaps below appear across all five reviewed platforms. They are not bugs — they are emergent consequences of the assumption that the agency owns the workspace. A platform that flips that assumption (project ownership = client) gets all twelve as a side-effect.

For each gap: the gap, why it persists, the case for closing it, and how Handoff addresses it.

---

## Gap 1 — Handover protocol (export/import)

**The gap.** None of the five platforms can export an SEO project as a portable, vendor-neutral bundle that another platform (or another agency on the same platform) can import. There is no `package.json` for an engagement.

**Why it persists.** Switching costs are revenue for incumbents. The agency-of-record model rewards lock-in.

**The case for closing it.** Brands lose 20–40% of organic traffic at every transition because there is no standard way to transfer audit history, decisions, link inventory, and baseline metrics. The first platform to publish a credible open spec wins the trust narrative.

**Handoff response.** The handover bundle is the core feature. It is a JSON-Schema'd file with twelve top-level objects (audit history, link inventory, disavow, content briefs, decisions log, redirect history, anchor strategy, vendor relationships, baseline metrics, roadmap, comments, meta). The spec lives in a separate repo and is intended to be vendor-neutral.

---

## Gap 2 — Asset escrow concept

**The gap.** Every platform treats credentials and assets as either "the agency has them" or "the agency doesn't". Nothing in between. There is no neutral holding state for the period between an outgoing agency stepping back and an incoming agency taking over.

**Why it persists.** Escrow is a trust pattern; trust patterns require a neutral third party. None of the existing platforms occupy that neutral position — they're tools the agency uses, not infrastructure both parties rely on.

**The case for closing it.** Atomic handovers are unsafe. Revoking the outgoing agency's GSC access on day 1 of a 30-day transition means losing emergency remediation capacity. Escrow lets both parties retain read-only access during a defined rank-safety window.

**Handoff response.** Every transferable asset carries one of three statuses: `TRANSFERRED`, `ESCROW`, `PENDING`. The escrow window is a contractual concept (typically 14–30 days), enforced by the platform's role-based access controls.

---

## Gap 3 — Project ownership = client (not agency)

**The gap.** In every reviewed platform the workspace is created under the agency's account. The agency invites the client into the agency's project. When the agency relationship ends, the project ends.

**Why it persists.** It mirrors the contractual reality of agency engagements — the agency *is* the customer of the SEO platform. Most platforms have no concept of brand-as-tenant.

**The case for closing it.** Inverting the model gives every brand a portable workspace. The agency becomes a guest with scoped, revocable access. When the brand fires the agency, it loses nothing.

**Handoff response.** Multi-tenant model where the project is owned by the brand by default. The agency is invited with a role (Admin / Editor / Viewer). One-click revocation removes the agency's access without touching the underlying project. UI badges throughout: "Owned by [Client] / Managed by [Agency]".

---

## Gap 4 — Marketplace of SEO contractors

**The gap.** None of the five platforms have an in-product marketplace where a brand can hire vetted individual SEO contractors (PMs, technical SEOs, link-builders, outreach specialists, content writers) with embedded billing.

**Why it persists.** Marketplaces require two-sided onboarding, vetting, payments infrastructure, and dispute resolution. They are an operationally expensive bet most tooling companies can't justify.

**The case for closing it.** When a brand fires an agency, hiring a single contractor is often the right next step but operationally heavy: finding a vetted person, contracting them, managing time, paying them, scaling them. A marketplace inside the SEO PM tool collapses this to "invite to project".

**Handoff response.** Marketplace MVP is a one-sided seeded directory in months 1–9 (30–50 manually vetted contractors). Two-sided marketplace with Stripe Connect, vetting (28-point check, Credo-style), LLM-based matching, and 12–15% take rate from month 18 onward.

---

## Gap 5 — Modular roadmap-builder from typed task-blocks

**The gap.** SE Ranking and SEOWORK have task lists; AgencyAnalytics has goals; Ahrefs and Semrush have neither. None have a *typed* task-block library — drag-drop blocks like "site audit", "internal linking review", "AI Overview optimisation", each with preconditions, success metrics, recommended roles, and dependency resolution.

**Why it persists.** Project management generalists (Linear, Asana, ClickUp) don't know the SEO domain; SEO platforms don't know PM. The intersection has been left to in-house spreadsheets.

**The case for closing it.** Most SEO work is recombinations of well-known plays. A drag-drop, SEO-aware Linear is what every agency PM is hand-rolling in Notion today.

**Handoff response.** Library of 60–80 typed task-blocks across four channels (SERP, Local/GEO, ASO, AI-search). Each block carries preconditions, success metrics, effort estimate, recommended role. Templates for "E-commerce SEO", "B2B SaaS SEO", "Local SEO", "AI-search ready". Drag-drop timeline view by quarter.

---

## Gap 6 — Outcome-tracking (expected vs actual on every task)

**The gap.** Only SEOWORK has a Plan/Fact mechanism with per-employee productivity scoring. Every other platform shows tasks completed; none show tasks *delivering on their promises*.

**Why it persists.** Outcome-tracking is hard. Outcomes are noisy. Attributing rank movement to a specific task requires rigorous baselines.

**The case for closing it.** "We did 47 tasks this month" is the report agencies write today. "We promised +12 positions on these 8 keywords; we delivered +9 on 6 and –1 on 2" is the report brands actually want.

**Handoff response.** Each task has an `expected_outcome` field (e.g., "+5 positions for kw X within 30 days"). The platform automatically measures `actual_outcome` after the time horizon. Per-contractor productivity score = aggregate of delivery-vs-promise across tasks.

---

## Gap 7 — SEO-team specific roles

**The gap.** All five platforms have generic roles: Owner, Admin, Editor, Viewer. None have SEO-specific roles like Technical SEO, Link-builder, Outreach, Content Strategist.

**Why it persists.** Generic roles are easier to ship. Vertical roles mean per-vertical maintenance.

**The case for closing it.** SEO teams are heterogeneous. A link-builder needs access to link inventory and outreach contacts but not to redirect history. A content strategist needs briefs and SERP context but not credentials. Generic roles force over-permissioning.

**Handoff response.** Five SEO-specific roles (PM, Tech SEO, Link-builder, Outreach, Content) with default permission sets calibrated to the work, plus the standard Owner/Admin/Editor/Viewer controls.

---

## Gap 8 — ASO integration

**The gap.** None of the five integrate App Store / Google Play / Huawei AppGallery data. ASO lives in entirely separate tools (AppTweak, MobileAction).

**Why it persists.** ASO is a different ecosystem with different APIs and different ICPs.

**The case for closing it.** Half of B2C SEO budgets at app-led brands are now ASO. Asking a brand to run two platforms in parallel — one for web, one for app — duplicates work and breaks cross-channel KPIs.

**Handoff response.** ASO module in Phase 2 (months 18–30). AppTweak / MobileAction API integration, ASO task-block library, support for App Store, Google Play, and Huawei AppGallery. Pricing as an add-on tier.

---

## Gap 9 — Cross-channel KPI aggregation

**The gap.** SERP, ASO, Local, and AI-search live in separate dashboards even when a single platform technically covers them. There is no single dashboard that tells a brand "this is your total visibility across channels".

**Why it persists.** Each channel was added at a different time, with different data models. Aggregation requires a unified abstraction.

**The case for closing it.** Brands report to boards in single numbers, not per-channel breakdowns. "Total visibility growth +14% QoQ" is more useful than "SERP +12%, ASO +18%, AI-search +6%, Local +9%".

**Handoff response.** Cross-channel KPI roll-up at the project level. Total Organic Visibility Score that aggregates SERP rankings, ASO download attribution, Local pack visibility, and AI-search citations into a single number, with drill-downs.

---

## Gap 10 — Switch-agency wizard

**The gap.** The most painful workflow in SEO — switching agencies — has no dedicated UI in any platform. It happens via tickets, spreadsheets, and recovery work.

**Why it persists.** No incumbent benefits from making it easy.

**The case for closing it.** A 3-step wizard (export bundle → revoke outgoing agency access → invite incoming agency) collapses six weeks of operational work into an afternoon.

**Handoff response.** The Switch-Agency Wizard is a Phase 3 feature: 3-step automated transition that emits a signed handoff bundle, sets escrow status on every asset, and provisions the incoming agency with appropriate role-based access. With audit-log entries on every step.

---

## Gap 11 — Audit trail for legal-grade handover

**The gap.** Audit logs in existing platforms are operational — "user X edited task Y at time Z". None are positioned for legal-grade evidentiary use during contract disputes.

**Why it persists.** Operational logs are sufficient for the agency-led use case. Legal-grade trails require append-only storage, signed events, and retention guarantees that drive up infrastructure cost.

**The case for closing it.** When a brand and an outgoing agency dispute "did the agency hand over the disavow file?", the answer should be a signed event in the bundle, not a sworn statement.

**Handoff response.** Append-only decisions log with cryptographic signatures on bundle contents. Per-asset transition history. Optional notarised export to PDF for use in contract disputes. (Conductor offers similar at $30k+; Handoff bakes it into the standard tier.)

---

## Gap 12 — Free public "Reality Check" tool

**The gap.** None of the five offer a free public tool that lets a brand audit its current agency without signing up.

**Why it persists.** Existing platforms sell to agencies. A "is your agency hiding things from you?" tool is hostile to the customer.

**The case for closing it.** It is a viral, viable wedge for brands who suspect they are being underserved but lack the data to prove it. Each Reality Check is a high-intent lead.

**Handoff response.** Free public Reality Check at `handoff-smooth-transitions.lovable.app/reality-check` (planned). Inputs: domain + read-only GSC/GA4 access. Outputs: 4-section report covering performance audit (rankings vs. promises), transparency audit (which data is being hidden), asset ownership audit (12-point check, 0–100 score), and transition risk score (what would break if the agency left tomorrow). Email-capture for the full report. PDF export.
