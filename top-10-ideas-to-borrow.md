# Top 10 ideas worth borrowing

Patterns the existing platforms got right. The competitive moats are in the *unfilled* cells of the feature matrix — but a new entrant still has to be table-stakes-good on the contested ones, and these are the patterns that set the bar.

## 1. AgencyAnalytics — Widget-builder + 80 integrations

Drag-drop widget grid, customisable per-client dashboards, native integrations to GSC, GA4, Ahrefs, Semrush, Stripe, and 75 others.

**How to adopt.** Copy the UX pattern. Don't try to copy the integration count from day one — that's a years-long project. Start with 8–10 critical integrations (GSC, GA4, Ahrefs API, Semrush API, Looker Studio, Stripe, Slack, the rest as priorities emerge).

## 2. AgencyAnalytics — "Ask AI" (natural-language queries)

The 2026 killer feature. Natural-language data queries: "How did organic traffic change last week versus prior?" returns a chart and a plain-English summary. Once you've used it, every other dashboard feels obsolete.

**How to adopt.** Anthropic API + a structured data layer over the project's metrics. Phase 3 feature — too heavy for MVP, but unmissable by the time you're past $1M ARR.

## 3. SE Ranking — Marketing Plan + task → tool deep-linking

Every task has a direct link into the relevant SEO tool with parameters pre-filled. Click "Audit canonicals" → land in the Audit tool with the right scope already loaded. Powerful productivity mechanic.

**How to adopt.** Bake it into every typed task-block in the modular roadmap. The block itself knows which tool it depends on and what parameters to pass.

## 4. SEOWORK — Plan/Fact with productivity score ⭐

Unique RU feature: when a task is created, user specifies the "expected outcome". After 30 days, the system measures the actual outcome. Per-contractor productivity-score = aggregate of delivery vs. promise across tasks.

**How to adopt.** Adapt to global context as **Outcome-Tracking**. Make `expected_outcome` a required field on task creation. Auto-measure after the time horizon. Surface productivity scores on contractor profiles in the marketplace. This is the single most important feature borrowed from anyone in this analysis — it's the difference between "tasks done" and "tasks delivered".

## 5. Ahrefs — Site Audit prioritisation (severity × type matrix)

Issues categorised by severity (Errors / Warnings / Notices) crossed with type (Critical / Important / Recommended). The matrix layout is the gold-standard for issue triage.

**How to adopt.** Copy directly into the audit module. The matrix should be the default view; lists are the secondary view.

## 6. Ahrefs — Brand Radar (AI-search visibility)

Track citations across ChatGPT, Gemini, Perplexity, AI Overviews. Share-of-voice across AI-search engines.

**How to adopt.** Embed into the modular roadmap-builder as first-class task-blocks: "Optimise for ChatGPT citation", "Track AI Overview presence", "Monitor Perplexity share-of-voice". The data layer comes from Profound/Peec API integrations — partner, don't rebuild.

## 7. Semrush — App Center (extensibility model)

Marketplace-based architecture. Third parties can add tools to the platform. Creates network effects and lock-in.

**How to adopt.** Late phase only (Phase 5+). Too heavy for MVP. Worth the wait — extensibility is what compounds platform value over five-plus years.

## 8. AgencyAnalytics — White-label client portal + per-client login

Standard for agency tools. Per-client logins, custom domain, agency branding. Well-executed in AgencyAnalytics.

**How to adopt.** Must-have from day one. Brand-side users need access without seeing the agency's other clients.

## 9. AgencyAnalytics — Goals + Alerts

Simple ROI tracking. "Set a goal: +20% organic traffic by Q3" → automatic monitoring + alerts on deviation.

**How to adopt.** Simple feature, high value. Ship in MVP. Notification channels: email, Slack, web, in-product.

## 10. Ahrefs — Bulk edit in Rank Tracker

Select multiple keywords → batch edit/delete/move. Productivity mechanic that the other platforms haven't quite matched.

**How to adopt.** Bulk-edit pattern wherever lists appear: keywords, tasks, links, vendors. Cmd-click selection, shift-click range selection, action toolbar at the top. Ship in MVP — once users have 100+ items in any list, single-row editing becomes unusable.

## What didn't make the top 10

- **Semrush Position Tracking historical depth.** Best-in-class, but the cost of replicating it doesn't pay off — partner with Ahrefs/Semrush via API instead.
- **SE Ranking's pricing tiers.** Aggressive pricing is a competitive weapon, not a UX pattern. The freemium tier is the right thing to copy here, not the per-seat ladder.
- **Ahrefs Content Explorer.** Powerful research tool, but adjacent to the PM/handover thesis. Skip until later phases.
- **Conductor's enterprise audit-trail.** Worth referencing in the legal-grade handover spec, but operationally too heavy for MVP.

The pattern across the top 10: copy the UX patterns that compound (Ask AI, outcome-tracking, bulk-edit), partner on the data layers that commoditise (rank tracking, backlink databases, AI-search citation feeds), build new on the gaps no one filled (handover protocol, asset escrow, marketplace).
