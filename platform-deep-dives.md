# Platform deep-dives

Field notes from hands-on time in trial / working accounts of all five platforms. What the sidebar looks like, what the strongest screen is, where the friction shows up.

---

## Semrush — the broadest platform

**Sidebar (11 categories).** Home / Keyword Research / SEO (Position Tracking, Site Audit, On-page SEO) / Domain analytics (Traffic, Backlinks) / Local SEO / Apps / Social Media / Advertising / Brand Monitoring / Content Marketing / App Center.

**App Center (61+ apps).** Categories: SEO, Social Media, Content, Advertising, AI Apps, Competitors, SMB, Mobile, Workflows, Ecommerce, Video, Brand, LeadGen, Toolkits.

Featured apps observed:

- **LLM Gap Analyzer** ($49/mo) — "Outrank competitors winning in Google AI and ChatGPT". New for 2026.
- SERP Gap Analyzer ($99/mo)
- AdClarity ($349/mo)
- CallRail ($125/mo)
- Influencer Analytics ($249/mo)
- Exploding Topics ($99/mo)

**Strengths.** 61+ tools in App Center; AI-search coverage via LLM Gap Analyzer and (formerly $99) AI Toolkit; massive backlinks/keywords database; SEO + PR + Social in one suite.

**Weaknesses.** Overload — 61+ apps is overwhelming on first contact. App Store model fragments billing (each app is its own subscription). Agency Growth Kit was sunset in 2025–2026, leaving no cohesive PM/CRM layer. No project lifecycle.

**What to copy.** App Center as an extensibility model — but only later. It's a network-effect lock-in mechanism that's too heavy for an MVP.

**What to skip.** The agency-management layer (already sunset). PPC research (out of scope for SEO-focused product).

---

## SE Ranking — the closest competitor on PM functionality

**Sidebar.** Dashboard / Keyword Research / SERP / Backlinks / Audit / Marketing Plan / Reports / Integrations.

**Strongest screen — Marketing Plan.** A flat list of SEO tasks with task → tool deep-linking: every task has a direct link into the relevant SEO tool with parameters pre-filled. Clicking "Audit canonicals" jumps straight into the Audit tool with the relevant scope. Powerful productivity mechanic.

**Strengths.** Best price-to-value on the global market ($65/mo entry). Marketing Plan is the closest existing thing to a roadmap-builder. Decent multi-client agency view. White-label client portal.

**Weaknesses.** Marketing Plan is a flat list, not a typed/templated roadmap. No outcome-tracking. No per-employee productivity scoring. AI-search support is built-in (good) but shallow compared to Ahrefs Brand Radar.

**What to copy.** Task → tool deep-linking. Bake it into every typed task-block: clicking a "site audit" block jumps into the audit module with the scope pre-set.

---

## AgencyAnalytics — the reporting/dashboards leader for agencies

**Sidebar.** Dashboards / Reports / Goals / Integrations / Clients / Team.

**Strongest screen — the widget-builder.** Drag-drop widget grid with per-client customisation. 80+ native integrations. Per-client logins on the white-label portal. Goals tracking with auto-monitoring and alerts.

**"Ask AI" feature (2026).** Natural-language data queries — "How did organic traffic change last week vs. prior?" returns a chart + a written explanation. This is a killer feature for the segment.

**Strengths.** Best-in-class reporting and dashboard UX. Largest native integration library. White-label client portal is the gold standard. "Ask AI" is genuinely useful.

**Weaknesses.** No native SEO data layer — every metric comes via integration. No site audit, no keyword research, no backlinks tool. The platform is a *report layer* on top of someone else's data.

**What to copy.** Widget-builder UX (drag-drop, per-client customisation), "Ask AI" (Anthropic API + structured data layer — Phase 3 feature), Goals + Alerts (simple, high-value).

---

## Ahrefs — the strongest SEO data + AI-search tools

**Sidebar.** Dashboard / Site Explorer / Keywords Explorer / Site Audit / Rank Tracker / Content Explorer / Brand Radar / SMM / Competitive Analysis / Reports.

**Strongest screen — Site Audit.** Issues are categorised by severity (Errors / Warnings / Notices) × type (Critical / Important / Recommended). The matrix layout is the industry gold-standard.

**Brand Radar (2026, $199/mo add-on).** Track citations across ChatGPT, Gemini, Perplexity, Google AI Overviews. Share-of-voice across AI-search engines. The current best implementation of AI-search visibility.

**Bulk edit in Rank Tracker.** Select multiple keywords, batch edit/delete/move. Productivity mechanic that the other platforms haven't quite matched.

**Strengths.** Best raw SEO data. Best site audit UX. Best AI-search visibility (Brand Radar). Power-user keyboard shortcuts and bulk edits everywhere.

**Weaknesses.** No project management at all. No tasks, no team roles, no outcome-tracking. It's a research and tracking tool, not a workspace.

**What to copy.** Site Audit prioritisation matrix (severity × type) into our audit module. Brand Radar as inspiration for AI-search blocks in the modular roadmap. Bulk edit patterns wherever lists appear.

---

## SEOWORK (RU/CIS) — closest PM philosophy for in-house teams

**Sidebar.** Projects / Tasks / Plan/Fact / Reports / Team / Settings.

**Strongest screen — Plan/Fact with productivity score.** Unique RU/CIS feature. When a task is created, the user specifies an "expected outcome" (e.g., "+5 positions for keyword X"). After 30 days, the system automatically measures the actual outcome. Per-contractor productivity score = aggregate of delivery vs. promise.

**Strengths.** The only platform with real outcome-tracking. Strong project lifecycle. Tasks tied to measurable goals.

**Weaknesses.** RU/CIS-only positioning. No global ICP. AI-search support absent. UI is dated relative to global competitors. No marketplace, no handover.

**What to copy.** **Outcome-tracking is the most important feature borrowed from anyone in this analysis.** Adapt it to global context: every task carries `expected_outcome` and `actual_outcome` fields, automatically measured. Per-contractor productivity score follows naturally.

---

## What I didn't get to

- **Conductor** — Enterprise tier ($30k+ ACV). Different ICP. Has the closest thing to legal-grade audit-trail features. Worth a second-pass review at the enterprise stage.
- **BrightEdge** — Same enterprise tier. Strong Data Cube; weak PM.
- **Botify** — Tech-SEO leaning enterprise. Excellent crawl data; minimal PM.
- **Lumar** (formerly Deepcrawl) — Crawler-led. Out of scope for the PM/handover thesis.
- **Clearscope, Surfer, MarketMuse** — Content-led tools. Adjacent rather than competitive.
- **Profound, Peec, Otterly, Brandwatch** — AI-search specialists. Worth integrating with rather than competing against.

These are flagged for future reviews as Handoff moves up-market.
