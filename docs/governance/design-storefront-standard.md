# CornerTech AI | Design & Storefront Experience Standard

**Version:** 0.1 (FOUNDER APPROVED DIRECTION, NOT YET ADOPTED IN REPOSITORY)  
**Prepared:** 2026-11-07  
**Candidate repository path:** `docs/governance/design-storefront-standard.md` in `Conquereleven/cornertech-ai`  
**Status:** FOUNDER APPROVED for corporate design direction on 2026-11-09 (ECOSYSTEM-DEC-002). Repository implementation and client release gates remain separate.  
**Applicability after separate adoption:** CornerTech-owned public websites, CornerOps client storefront projects, and CornerTech Commerce storefront templates/runtimes. Client repositories must adopt the standard explicitly and retain their stricter product-specific rules.

## 0. Authority, inheritance and non-goals

This is a **specialized design and storefront quality supplement**, not a replacement for:

- `docs/governance/execution-standard.md` (Execution Standard 1.0; canonical task states, verification and approval);
- `docs/governance/world-class-operating-standard.md` (CT-WCOS v1.1, adopted by PR #109 on 2026-11-03; stale agent-reference wording corrected by PR #110 on 2026-11-08);
- `AGENTS.md`, `frontend/AGENTS.md`, security/permission/release requirements and active client-specific contracts.

Where rules conflict, the more restrictive applicable security, Founder-approved, client or release rule prevails. **One control. One evidence. One approval.** Do not duplicate validations, re-run already accepted reviews without a material change, or claim a draft is adopted.

This standard does **not** authorize commits/pushes, pull requests, merges, deployments, DNS changes, infrastructure, payment integrations, customer-data access, content publication, asset copying, or use of a client's brand.

## 1. North star: signature craft, measurable usefulness

> Every interaction must earn its cost in attention, performance and complexity by helping a user understand, decide, trust, navigate or act.

CornerTech's design ambition is distinctive, editorial, precise and accessible. It must **not** be reduced to dark mode, glass, oversized typography, bento grids, autoplay video or animation density. A beautiful screen that causes purchase friction is not excellent storefront design.

The experience must have one identifiable brand point of view while maintaining semantic navigation, visible actions and dependable use on a mid-range mobile device. Originality is a requirement; third-party layouts, code, art, copy, trademarks or videos require proper permission or independent creation.

## 2. Context-first design contract

For any substantial new surface, capture the following in the existing issue/PR rather than generating another report:

1. **Audience/job:** user, intent (discover / compare / buy / operate / seek support), key task, device/connection assumptions.
2. **Product class:** A) brand/campaign, B) marketing/agency, C) storefront browse/product/cart/checkout, or D) merchant/operations dashboard.
3. **Business action:** one primary user outcome; truthful supporting content and stage of product maturity.
4. **Constraints:** current repo/framework/brand/assets/design tokens, architecture, tenant boundaries, locale, accessibility, legal or client controls.
5. **Design reference breakdown:** cite a reference for its *mechanism and purpose*, not an instruction to clone it.
6. **Acceptance evidence:** selected visual target, mobile/desktop screenshots, interactions, performance/accessibility tests, owner and exact approval boundary.

**Never require a particular framework merely because an inspirational prompt names it.** Preserve the target repository's adopted framework and architecture unless a separately reviewed architecture decision approves a change.

## 3. Design-system architecture and brand sovereignty

### 3.1 Token layers

Use semantic tokens for color, typography, spacing, radius, elevation, focus, breakpoints and motion. Map them into a product-specific theme. No shared hardcoded brand palette. Recommended *roles* include:

- `color.canvas`, `color.surface`, `color.text.primary`, `color.text.muted`, `color.action.primary`, `color.focus`, `color.border`, `color.status.*`;
- `type.display`, `type.heading.*`, `type.body`, `type.label`, `type.mono`; fluid sizing where appropriate;
- `space.*`, `radius.*`, `elevation.*`, `motion.duration.*`, `motion.easing.*`;
- `material.solid`, `material.translucent`, `material.glass-control` as optional semantic treatments.

The source of truth is the product's current stylesheet/token package. New tokens must be versioned/mapped and have light/dark and responsive states where relevant. Do not silently replace existing CornerGlass, tenant palettes, or accepted component signatures.

### 3.2 Shared primitives vs. individual client brand

Share **behavioral contracts and tested components** when justified (accessible menus, buttons, cart badge, price presentation, product filters, status messages, media loading, empty/error states). Keep each tenant's typography, tone, imagery, visual signature and token values independent. A shared product runtime may expose a typed theme/config interface. Avoid per-tenant branches or duplicated logic where configuration is sufficient, but do not force identical branding.

Client isolation includes assets, analytics, product catalogs, pricing, credentials, customer data, orders and rendering context. A shared frontend does not imply shared client records.

## 4. Signature interaction decision policy

Select **at most one dominant expressive interaction per page by default**. Supporting micro-interactions should be restrained. This is a heuristic, not a study-derived optimum. Prefer zero heavy effects on commerce checkout and operational screens. A second major effect needs explicit user value, fallback and performance evidence.

| Interaction | Brand/campaign | Storefront | Operations UI | Guardrail |
|---|---|---|---|---|
| Text reveal / scramble | Selective | Optional on short hero only | Avoid | Keep literal HTML text, <= ~1s, reduced-motion static |
| Scroll-synced index | Excellent for long stories | Useful only for lengthy editorial catalogs | Rare | Real anchor links, aria-current, compact mobile counter |
| Drag-to-explore canvas | Optional for discovery | Optional alternate *experience* view | Avoid | Always offer conventional searchable/filterable grid |
| View switch (experience/grid) | Helpful | **Strong candidate** | Useful when task warrants | Preserve state, focus, filters and access to products |
| Real-world product toggle (e.g. light on/off) | Good | **Strong when it answers a buying question** | Product-specific | Accurate images, label before/after, accessible control |
| Branded preloader | Only if genuine loading is unavoidable | Do not add artificial delay | Do not add artificial delay | Real progress if shown; no fake percent |
| Horizontal or scroll-masked storytelling | Campaign narrative | Optional editorial landing; not catalog/checkout | Avoid | Never hijack wheel, scroll or keyboard; reduced-motion fallback |
| Cursor material/WebGL reveal | Exceptional campaign only | Avoid default | Avoid | Progressive static fallback, cap DPR, battery/GPU tests |
| Live 3D hero/playable portfolio | Exceptional proof-of-craft work | Not a default commerce pattern | Avoid | Isolated lazy module, responsive fallback, performance review |
| 404 mini-game | Optional for creative showcase | Avoid | Avoid | Home/search/help routes must be prominent |

**Evidence label:** The two Design Shop PDFs describe design mechanisms and illustrative sites, not a controlled conversion or usability experiment. They are reference material, not measured impact proof.

## 5. Liquid Glass / CornerGlass material policy

### 5.1 Scope

Apple's Liquid Glass is a native dynamic material in platform UI frameworks; a web component built from CSS is an **approximation**. Do not label a web CSS approximation as official Apple Liquid Glass implementation. CornerGlass is CornerTech's existing accepted visual identity in applicable surfaces. Do not replace it by default.

Use restrained glass-like treatment primarily on **floating functional layers**: site navigation, compact toolbar, contextual menu, drawer handle, filter chip or high-value overlay. Default cart, pricing, long-form text, stock states, product cards and checkout forms to solid or opaque surfaces with reliable contrast. Avoid glass-on-glass stacking.

### 5.2 Implementation tiers

- **L0, always:** solid accessible fallback with correct hierarchy and contrast.
- **L1, web default:** translucent color + border + optional `backdrop-filter: blur(...) saturate(...)` guarded with `@supports`. Respect `prefers-reduced-motion`; accommodate reduced transparency where supported and provide an explicit high-opacity fallback regardless of media-feature support.
- **L2, experimental:** masked highlights, SVG filters or GPU shaders only for approved campaign proofs with testable value, cleanup, fallback and performance budget.
- **Native Apple apps:** use supported SwiftUI/UIKit/AppKit platform APIs where suitable; this policy does not require recreating them in web canvas.

Avoid non-consensual audio, aggressive glowing gradients, large moving distortions beneath text or untested Safari fallback. Re-evaluate under real product imagery, light and dark scenes, keyboard focus, zoom and device settings.

## 6. Motion rules and technology selection

| Need | Default candidate | Use condition |
|---|---|---|
| Hover/focus, basic reveal, feedback | CSS transitions / browser-native APIs | No JS library when unnecessary |
| React gestures, layout transitions, transient state | Motion for React (`motion/react`) | Existing stack compatible; no redundant animation ownership |
| Complex cinematic timelines, pinned editorial scenes | GSAP / ScrollTrigger | Approved brand/campaign route, controlled lifecycle and measurable cost |
| Browser-native view transitions | Native View Transitions or React 19.3 support if already adopted | Progressive enhancement and routing compatibility checked |
| Live 3D | Three.js/WebGL | Exceptional approved story; no default dependency in commerce shell |
| HLS delivery | `hls.js` only where HLS actually required and native playback unavailable | Poster/static fallback and streaming proof; no compulsory HLS for normal videos |

No project should add GSAP + Motion + Three.js + HLS merely to satisfy an inspirational landing-page prompt. If both GSAP and Motion are used, they must not animate or control the same DOM property/node without a deliberate integration plan.

Existing product-specific animation choices remain authoritative. For example, an approved CornerTech public-site motion treatment with finite <=400 ms animations must not be replaced by a looping marquee. Long-form editorial stories can consider longer duration only as an explicit scoped exception with justified user value.

Default animation behavior: visual clarity first, no mandatory wait, no perpetual attention theft, clean unmount, stable layout, pointer/touch/keyboard equivalence, no scroll-jacking. For reduced motion, content and functionality remain complete without animation.

## 7. Commerce-first functional design gates

The purchase journey has priority over spectacle:

- **Discovery:** clear search, categories, sorting/filtering where catalog size justifies them, actual inventory/product images, meaningful alt text and descriptive links.
- **Product page:** truthfully present name, price, pack/variant, availability, quantity, allergens/materials as relevant, delivery/returns, primary Add to Bag and customer support. Maintain responsive sticky CTA only when it avoids occlusion.
- **Cart:** clear editable quantities, subtotal, shipping/tax caveats, stock changes, errors, recovery and safe empty state.
- **Checkout:** clean keyboard and touch interaction, accessible errors, valid delivery details and price transparency; never hide payment/reliability failures behind loading effects.
- **Trust:** authentic reviews/cases only, no fake countdowns, fabricated availability or unapproved client claims. Price and promotional copy require a real source/approval.
- **Operational integration:** Merchant dashboard, OMS, invoicing and payment workflows must prioritize data clarity, stable navigation and recoverable actions.

For client storefronts, do not transfer production identities or data between tenants merely to reuse design/code. The source storefront may be implemented in a separate repository and integrated through approved adapters, not duplicated backends by default.

## 8. Accessibility, responsiveness and real-device acceptance

Minimum applicable objective: WCAG 2.2 AA, with actual checks for text contrast >=4.5:1 (ordinary text), >=3:1 large text and relevant non-text/focus components; semantic headings and landmarks; labels; keyboard navigation; visible/unobscured focus; clear error recovery; target sizing and no critical horizontal overflow. Do not assume glass blur creates sufficient contrast.

Review at 320/375 px mobile, representative tablet (~768 px) and desktop (~1280/1440 px); 200% text zoom and 400% reflow when relevant; reduced motion; no WebGL; touch and keyboard. The exact viewport plan may follow stricter existing acceptance rules. Screenshot proof should cover hero, a representative product grid, product detail, cart/checkout or merchant view, and critical loading/error/empty state as appropriate.

## 9. Performance, instrumentation and acceptance evidence

**User-experience target:** Core Web Vitals good at the 75th percentile of real visits wherever field data is available: LCP <=2.5 s; INP <=200 ms; CLS <=0.1. CornerTech can use CLS <=0.05 as an aspirational internal target for new design work. A laboratory Lighthouse run is diagnostic, **not proof of p75 field performance**. Treat 3G/low-end or mid-range phone claims as test conditions to report, never measured facts without a run.

- Optimize above-the-fold content and image dimensions; reserve image/media space and avoid layout shift.
- Use video posters and appropriate resource priority; do not force a 3-second loader. Defer nonessential animation/media/3D modules, and provide reliable no-video/no-WebGL states.
- Evaluate meaningful content and conversion events only after privacy/analytics authorization; distinguish measured outcomes from design hypotheses.
- Monitor revenue-facing core journeys with functional and negative tests proportional to risk.

A P0 blocker includes a broken critical commerce path, client/tenant data exposure, misleading claims, severe accessibility regression or unauthorized production effect. A failed required check is not waived by a visual score.

## 10. Approval sequence and evidence receipt

Use existing ticket/PR. Apply Execution Standard 1.0 states unchanged.

1. **PREPARED:** current branch/SHA and source instructions, customer/task outcome, approved scope, visual target, planned tests, data/production boundaries.
2. **EXECUTED:** file paths and exact implementation SHA, preview URL or local rendering, library/assets sources and any side effects.
3. **VERIFIED:** reproducible desktop/mobile screenshots; accessible keyboard + reduced motion + no WebGL; relevant functional positive/negative journey tests; performance evidence with test conditions; peer review at exact SHA where risk warrants it.
4. **CLOSED:** required Founder/client visual and functional acceptance and separate release approvals documented; unresolved limitations have owner.
5. **BLOCKED:** reproduce missing capability/failing test and name the smallest safe unblock.

**Independent review:** For substantial template changes, checkout and shared multitenant primitives, one agent implements and the other reviews the exact SHA. Keep a single DRI and avoid redundant cross-review loops. A new visual standard itself requires Founder approval before repo adoption.

## 11. Reference-prompt contract for agents (copy, adapt, don't clone)

```text
TASK: Design and/or implement [specific surface] in [repository] on [branch] at [base SHA].
OUTCOME: [user's single primary task and observable business benefit].
DESIGN REFERENCE: [links/screenshots]. Extract interaction principles, not copied code/assets/layout.
BRAND: Preserve [current theme/tokens/typography/approved identity], distinct from references.
ARCHITECTURE: Inspect AGENTS.md, Execution Standard 1.0, CT-WCOS and local gates.
Preserve current framework, routes, contracts, tenant boundaries, data flows and client approvals.
SCOPE: [explicit included paths/flows]; EXCLUDE: [production, DNS, payment, real data, unrelated redesign].
UX: State hierarchy, mobile entry point, CTA, visible price/status/trust details, empty/error states.
MOTION: One meaningful signature interaction only if justified; progressive static/reduced-motion fallback.
MATERIAL: Optional restrained glass control layer; no glass-on-glass or content-obscuring cards.
PERFORMANCE: Run relevant build/test checks; report LCP/INP/CLS evidence type and conditions.
ACCESSIBILITY: WCAG 2.2 AA relevant checks; keyboard, focus, 320 px, zoom, touch.
EVIDENCE: Exact SHA, screenshots at representative widths, tested core journey, failed/untested checks.
REVIEW: Reviewer [Codex or Claude Code] independently reviews exact SHA when required.
OUTPUT: Working inspectable preview, concise disposition and approval still needed.
NO PUSH, PR, MERGE, DEPLOYMENT, DNS, PAYMENT OR REAL-DATA ACTION without exact Founder GO.
```

## 12. Reference library and provenance

**User-supplied design references:**

1. `Interactions-That-Feel-Premium-Part-III-Full-Breakdown-2026-07-11-11-47-55.pdf`, The Design Shop, *Interactions That Feel Premium, Part III*, 11 pages. Especially pp. 2-10: seven patterns, skip/use conditions and delivery checklists.
2. `premium-field-notes-2-2026-27-10-11-31-19.pdf`, The Design Shop, *Interactions That Make Websites Feel Premium, Part II*, 5 pages. Especially pp. 2-4: discovery/grid modes, progress and product-demo interaction.
3. User-supplied HYLIOX recreation prompt, Nov. 7, 2026: visual and implementation reference, **not** an authority on Hyliox's current website or business terms.

**External implementation and UX evidence:**

- [Apple HIG: Materials and Liquid Glass](https://developer.apple.com/design/human-interface-guidelines/materials)
- [Apple Developer: Liquid Glass technology overview](https://developer.apple.com/documentation/TechnologyOverviews/liquid-glass)
- [MDN: backdrop-filter](https://developer.mozilla.org/en-US/docs/Web/CSS/backdrop-filter)
- [MDN: reduced transparency (limited support)](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-transparency)
- [Google: Core Web Vitals](https://developers.google.com/search/docs/appearance/core-web-vitals)
- [web.dev: Video performance](https://web.dev/learn/performance/video-performance)
- [Motion for React](https://motion.dev/docs/react)
- [React 19.3 release](https://react.dev/blog/2026/09/09/react-19-3)
- [Baymard: Product list and filtering UX](https://baymard.com/research-articles/current-state-product-list-and-filtering)
- [Brad Frost: Atomic Design](https://atomicdesign.bradfrost.com/outline/)

**Policy source as inspected (read-only, 2026-11-07):**

- [Corporate AGENTS.md](https://github.com/Conquereleven/cornertech-ai/blob/main/AGENTS.md)
- [Execution Standard 1.0](https://github.com/Conquereleven/cornertech-ai/blob/main/docs/governance/execution-standard.md)
- [CT-WCOS v1.1 adopted standard](https://github.com/Conquereleven/cornertech-ai/blob/main/docs/governance/world-class-operating-standard.md)
- [Frontend AGENTS.md](https://github.com/Conquereleven/cornertech-ai/blob/main/frontend/AGENTS.md)

## 13. Proposed first pilot and next approval

**Pilot:** A reversible local design comparison in Hungry Guru (current approved hybrid hero + quick purchase) or a dedicated CornerTech Commerce component lab, *only after source state and current branch/preview are rechecked*. Do not rewrite 3L production or Golositalia payment flows to test aesthetics. Compare existing vs optional L1 glass on navigation and a functional product experience/gallery toggle. Evaluate task completion, no regression in Add to Bag, mobile screenshots, contrast and loading cost. No production release is implied.

**Founder's decision:** APPROVED as corporate design direction on 2026-11-09 under ECOSYSTEM-DEC-002. Technical repository adoption, per-client usage and any PR/merge/deployment remain separately governed. The original proposal is preserved unchanged; this file is the Founder-approved annotated version.


## Corporate publication note · 2026-11-09

Founder-approved direction under ECOSYSTEM-DEC-002 is proposed for repository adoption in Draft PR #111. This does not auto-adopt the standard in client repositories or authorize copying designs/assets, client releases, production or infrastructure. Any historical statements describing CT-WCOS v1.1 as *proposed* are superseded: CT-WCOS v1.1 was adopted in corporate `main` through PR #109 and its references corrected in merged PR #110.
