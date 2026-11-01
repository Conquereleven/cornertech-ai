# CornerTech AI · World-Class Operating Standard (CT-WCOS) v1.0

**Corporate decision:** Approved by the Founder & CEO on 2026-10-26.  
**Repository adoption:** Proposed on a separate branch; this file does **not** become an effective repository instruction until its PR is reviewed and merged with the required Founder approval.  
**Scope:** Design, engineering, product, innovation/AI, and execution.  
**Source:** The Founder's internal benchmark research, "CornerTech AI — Benchmark del 1% mundial y estándar operativo de clase mundial" (2026-10-26), and the approved internal CT-WCOS v1.0. The full research remains private. This is the compact, public-safe agent contract, not a reproduction of that research.

## 1. Policy hierarchy and authority

- [Execution Standard 1.0](execution-standard.md) remains the **single canonical repository policy for execution, accountability, delivery states, evidence and closure**. CT-WCOS adds a cross-functional quality bar; it does not fork or replace the execution standard.
- [Permissions](../security/permissions.md), [human approvals](../security/human-in-the-loop.md), local `AGENTS.md` files, client/tenant isolation, release contracts and applicable law remain in force. The stricter boundary wins.
- No document grants an agent permission to send messages, alter customer data, spend money, merge, deploy, change credentials or infrastructure, or bypass an existing approval gate.
- The aspiration to be world-class is **not** a verified statistical claim that CornerTech ranks in the world's top 1%. Do not make such public claims without evidence.

## 2. Operating model

| Role | Accountable responsibility | Boundary |
| --- | --- | --- |
| Founder & CEO (human) | Final business and critical technical decisions, budget, approvals, production and customer-facing acceptance | Must approve gated actions |
| ChatGPT | Strategy, product framing, operational coordination, decision records and handoffs | Cannot claim another agent acted without evidence |
| Claude Chat / conversational Claude agents | **Virtual CTO:** architecture, technical direction, tradeoffs, standards, risk review and recommendations | Advisory, not a human corporate officer; not Claude Code; cannot self-approve |
| Claude Code | Peer engineering implementer: code, tests, documentation, evidence and independent review of another implementer's work | No automatic permission or self-review |
| Codex | Peer engineering implementer: code, tests, documentation, evidence and independent review of another implementer's work | No automatic permission or self-review |

Claude Code and Codex have equal implementation standing. Assign **one DRI per outcome**, clear file/resource ownership and an independent reviewer where required. A reviewer must assess the exact SHA and actual evidence. Claude Chat may challenge a design or recommend a decision, but it is not a substitute for an independent implementation review or Founder approval.

## 3. Five quality pillars

### A. Design and experience

- Create an original visual and interaction point of view, not an interchangeable AI-generated template or a copy of a reference company.
- Make hierarchy, language, information architecture, navigation, and next actions understandable.
- Treat mobile, keyboard/focus, semantic structure, contrast, reduced motion and critical UI states as core quality, not polish.
- Use motion only when it communicates meaning; provide accessible static fallbacks.
- Verify visual quality at representative desktop and mobile viewports, including text wrapping, overflow, loading, error and empty states.

**Gate:** coherent design rationale, accessible responsive states, reviewable prototype or implementation evidence, and explicit unresolved findings.

### B. Engineering

- Record material architectural decisions and alternatives with concise ADRs, including security, reversibility and operational tradeoffs.
- Test critical logic, integrations/contracts, main user journeys and negative security cases proportionally to risk.
- Apply least privilege, privacy and tenant isolation by design; threat-model authentication, payments, customer data and agent tool use.
- Provide observability, safe error handling and rollback/fallback where the change can affect users or operations.
- Prefer maintainable shared contracts and golden paths to unreviewed one-off patches.
- Establish baselines before setting performance, delivery or reliability targets. Never invent DORA, SLO or performance measurements.

**Gate:** exact SHA, relevant positive and negative tests, security/regression evidence, reviewer disposition and operational risk/rollback.

### C. Product

- Identify the user, problem, current workflow, desired outcome, constraints and measurable success before substantial implementation.
- Distinguish **verified customer evidence** from assumptions and hypotheses.
- Choose the smallest scope that delivers a coherent excellent outcome; avoid feature volume as a proxy for value.
- Keep a truthful product-status ledger: **VERIFIED / IN DEVELOPMENT / PROPOSED**.
- Instrument outcomes and collect real feedback after authorized release.

**Gate:** testable acceptance criteria, clear outcome and evidence/hypothesis provenance, owner and approval boundaries.

### D. Innovation and AI-native systems

- Explain the concrete workflow improvement and why AI/automation is appropriate.
- Define agent authority, human handoffs, tool permissions, failure modes and fallback behavior.
- Evaluate agents across **Outcome, Process, Quality and Efficiency**; test failure paths, injection risks, unsafe tool use and data exposure where relevant.
- Version prompts, models, tools and evaluation datasets when practical; report known limitations.
- Preserve reusable interfaces, evaluations and engineering learnings.

**Gate:** demonstrated value, relevant evaluations, safety boundaries, human control and recoverability.

### E. Execution and learning

- Use **context → dissent → decision owner → decision → commit → evidence**.
- Preserve the existing **PREPARED → EXECUTED → VERIFIED → CLOSED** lifecycle, with **BLOCKED** for an evidenced obstacle.
- Keep one accountable DRI and precise handoffs; task creation, a PR, green CI, a deploy or an agent message is not closure.
- Document risks, reviewer identity, reviewed SHA, evidence, approval and follow-up owner.
- Capture meaningful ADRs, incidents, lessons and approved exceptions without producing redundant bureaucracy.

**Gate:** real acceptance evidence in the relevant environment and explicit human acceptance wherever required.

## 4. Minimum task contract and gates

Every material task/PR must make these discoverable in its existing record:

1. **Outcome and DRI:** user/business result, owner, hypothesis or supporting evidence.
2. **Authorized scope:** affected paths/resources, environment, excluded work and applicable permissions.
3. **Acceptance:** measurable positive and negative tests, UX/accessibility/security checks when relevant.
4. **Implementation evidence:** exact commit SHA, artifacts, test commands/results, timestamps and target-environment limits.
5. **Independent review:** reviewer, exact SHA, findings, PASS/FAIL/HOLD; or an explicit note that independent review has not happened.
6. **Risk and decision:** rollback/fallback, open risks, required Founder/customer approval, actual state and next owner.

**Definition of Ready:** outcome, DRI, scope, environment, criteria, risks and approvals are understood before execution.

**Definition of Done:** required behavior is actually verified; evidence is inspectable; security/privacy/accessibility and rollback are addressed according to risk; independent review and Founder acceptance have occurred where required; remaining work has a named owner. A merged PR is not automatically Done.

**Severity:** P0 = automatic HOLD for critical security/privacy/tenant, false claims, major accessibility or unauthorized production risks. P1 = REVISE/BLOCK for unmet essentials, absent required independent review or inadequate evidence. P2 = documented non-blocking follow-up with owner. An average quality score never overrides P0.

## 5. Initial adoption and explicit exclusions

- **First adoption surface:** this repository, via a reviewed PR modifying only policy documents and agent entrypoints. The existing Execution Standard stays intact.
- **First quality pilot:** Website 3.0 design-first review, **not** authorization to code, merge or deploy. Preserve the stable Website 2.0 release and truthful labeling of Commerce as in development.
- **Other repositories:** inspect ownership, customer boundaries, current instructions and risk first; adopt individually through their own approved changes. No automatic propagation.
- **Pricing/unit economics:** remain HOLD until separate Founder approval.
- **No automatic agency:** this file does not assign work to Claude Chat, Claude Code or Codex. Each requires a real task in its available execution environment.

## 6. Versioning and exceptions

Changes to CT-WCOS require a versioned proposal, impact/risk note, review and Founder decision where material. Log exceptions with rule, justification, mitigation, owner, expiry and re-review date. Preserve existing, stricter local policies.

**Approval record:** Founder GO, 2026-10-26, to adopt CT-WCOS v1.0 corporately and **prepare repository integration without merge or deployment**. Repo adoption remains pending independent review and separate merge approval.
