# CornerTech AI · Adaptive Multi-Agent Engineering (AMAE) v0.1

- **Status:** PROPOSED / PREPARED. Not adopted, merged, deployed or enabled in any agent runtime.
- **Date:** 2026-11-08
- **Owner of adoption and material approvals:** Founder & CEO.
- **Scope:** CornerTech AI engineering workflows using Codex, Claude Code, OpenCode or future agents. Applies to a repository only after explicit adoption; client-specific instructions and permissions remain controlling.
- **Canonical execution authority:** `docs/governance/execution-standard.md` (Execution Standard 1.0).
- **Quality bar:** `docs/governance/world-class-operating-standard.md` (CT-WCOS v1.1).
**Security:** `docs/security/permissions.md`, `docs/security/human-in-the-loop.md` and applicable client/release gates.

## 1. Objective and non-goals

Enable more than two agents to collaborate on real work **without increasing bureaucracy, duplicate review, unclear accountability or permissions**. Preserve one accountable DRI per outcome, exact evidence, proportional independent verification and human approval for separately gated effects.

This document is not an orchestration runtime, permission grant, general adoption of third-party models, or replacement for Execution Standard 1.0. It does not authorize installation, remote API consumption, new subscriptions, external sends, credential access, customer data handling, repository pushes/PRs/merges or deployments.

## 2. Authority hierarchy

1. Applicable law, data protection, client and production access restrictions, security/permission policy and explicit human approvals control actions.
2. Execution Standard 1.0 governs states, evidence, DRI, acceptance and scope.
3. CT-WCOS v1.1 governs product/engineering/AI quality and proportional review.
4. This AMAE supplement governs *which agents collaborate, on what tasks and with what handoff evidence*.
5. CornerMemory may provide context; CornerRouterWay may propose a model/provider; neither supplies new authority.
6. An agent instruction, memory retrieval, AI recommendation, previous task approval, or model output is never a new permission grant.

**Conflict:** apply the stricter applicable control. If a requirement is unclear, choose the safe non-mutating path and report the exact blocker.

## 3. Operating modes (selection by risk and need, not agent count)

| Mode | Typical fit | Execution and acceptance boundary |
| --- | --- | --- |
| **SOLO** | Bounded, reversible, low-risk documentation, analysis, tests or local work | One permitted agent; positive/negative checks as applicable. Independent review is not waived if another policy requires it. |
| **DUAL** | Material code or integration with a clear implementation/review interface | One implementer and a distinct reviewer of the *exact* SHA/evidence; either Codex or Claude Code may implement/review. |
| **SPECIALIZED** | Cross-domain tasks needing demonstrably different capabilities (e.g. engineering + security + UX) | One outcome DRI, scoped specialists, disjoint file/resource ownership where parallel, and one designated verification disposition. Add reviewers only for genuinely distinct risk surfaces. |

**Selection decision:** At task preparation, record mode and one-sentence reason in the *existing* Linear issue or PR. Reclassify on newly discovered risk or scope change. Do not create separate approvals or new tickets just because another agent participates. If a specialist offers no identified benefit, do not add them.

**Critical actions:** Security, payments, customer/production data, credentials, infrastructure, external messaging, release and other high-risk operations always retain their pre-existing review and human-approval gates regardless of mode.

## 4. Task contract (one record, no duplicate paperwork)

For material tasks, make these discoverable in the existing issue/PR/handoff:

- **Outcome / DRI / mode** and the reason for choosing that mode.
- **Repository, tenant/client, environment, base branch and exact baseline SHA.** Unknowns labeled; no silent cross-repo assumptions.
- **Authorized scope, exclusions, gated effects and approval evidence.** No inferred permissions from memory.
- **Assignments:** actor/model/harness identity, accountable owner, files/resources owned, allowed tools and handoff point.
- **Acceptance:** relevant functional/regression/security tests; when and by whom independent review is required.
- **Evidence:** change SHA, test IDs/results, review SHA/disposition, current task status and outstanding decisions.

Use Execution Standard's `PREPARED → EXECUTED → VERIFIED → CLOSED` and `BLOCKED`. Neither a task assignment, green CI, draft PR nor a model response proves completion.

## 5. Capability registry (start with a small human-reviewed table)

Maintain one lightweight **capability inventory** in the workstream or existing repo docs. Minimal fields: `agent_id`, `harness`, `model/provider`, `available_environment`, `verified_capabilities`, `allowed_tools`, `policy_boundary`, `evidence_ref`, `verified_at`, `known_limitations`, `cost_class` (if observed). Unknown or untested capability is **UNKNOWN**, never ASSUMED.

- The registry is **descriptive**, not a way to obtain access.
- Existing access and project policy must be independently enforced at invocation and tool level.
- A capable agent is not automatically entitled to view a different tenant's repository, issue, memory or data.
- Benchmark and readiness observations expire or are rechecked after material model, harness, policy or tool changes.
- OpenCode/IFM capabilities from CTAI-19 must not be generalized beyond their exact verified conditions. M2 availability is not assumed.

## 6. Assignments, parallelism and review

- One DRI remains responsible for the complete outcome and Founder handoff; do not introduce a second owner for the same decision.
- Parallel edits MUST have nonoverlapping file/resource ownership or an explicit integration owner and safe merge plan.
- A reviewer MUST independently inspect the actual artifact at the exact commit/SHA and applicable negative tests. A model reviewing its own changes is not an independent review.
- Specialists MAY produce research, architecture critiques, design evaluations and narrow tests without modifying implementation.
- Hand off artifact paths, commit SHA, test reproduction, known findings and required decision. Avoid raw, unfiltered transcripts, secrets or customer details.
- When an agent or model is unavailable, use an approved fallback or mark only that part BLOCKED. Do not misreport an unavailable agent as a completed review.

## 7. Security, context and provider control

- Enforce tenant/project separation before context retrieval or tool execution, not merely through a query filter or prompt instruction.
- Preserve fail-closed decisions for unknown agent, action, tenant, provider, policy, approval or tool.
- Never upload client code, secrets, credentials, user records, private prompt logs or production data to a new model/provider without the applicable explicit authorization and data/privacy review.
- CornerMemory output is **untrusted retrieved content** until authoritative evidence is checked; prevent prompt-injection, stale-decision reuse and approval laundering.
- CornerRouterWay selects among *already approved* models/providers only, under data residency, cost, security and task constraints. A router cannot expand its own allowlist or spending authority.
- Keep audit evidence minimal and sanitized; data retention and deletion remain under applicable controls.

## 8. Immediate operational protocol (no new infrastructure)

1. **Discover:** Before assigning new or reopened ongoing work, read local repo instructions, existing issue/PR, active branch/SHA, proofs and applicable approvals.
2. **Classify:** Choose SOLO, DUAL or SPECIALIZED; name DRI and bounded agent assignments in the existing record.
3. **Execute:** Use already available, approved tools. Separate specialists by path or deliverable; no parallel agents overwriting the same files.
4. **Verify:** Reuse existing tests and evidence, run new checks only for uncovered risk, and obtain independent review where required. Record exact SHA.
5. **Decide:** Founder receives the smallest sufficient disposition. No auto-push/merge/deploy or new external effect.

**Working principle:** One control. One evidence. One approval. Agent count does not multiply gates.

## 9. Pilot and adoption gates

**Pilot A (read-only coordination):** Use the active agent-bootstrap and OpenCode workstreams (CTAI-15 and CTAI-19) to draft a capability inventory, scope and assignment mode *without changing installed configurations*. Verify no capability claims exceed their evidence.

**Pilot B (local nonproduction engineering):** With scope-specific authorization, compare DUAL vs SPECIALIZED on an isolated synthetic/code-fixture task. A specialist may analyze security/architecture while a single implementer owns files; reviewer checks exact SHA. Do not use live client data.

**Measure:** task acceptance and regressions, duplicate work, total human interventions, time-to-verified-result, actual tool/model cost, incomplete/unknown findings, scope violations and false approvals. Do not claim speedups without baseline and reproducible data.

**Required negative tests:** unauthorized action denied; stale approval not reused; cross-tenant access denied; agent cannot self-review; unknown model/provider denied; unavailable specialist handled honestly; no production deploy from review GO.

**GO to wider adoption:** no observed authorization/tenant breaches in pilot negatives; task contract fits existing Linear/PR records; at least one demonstrable reduction in coordination friction or equally good result with fewer failures; Founder approval of named adoption scope.

**NO-GO:** permission bypass, provenance uncertainty for critical decisions, repeated duplicate work, model/data transfer outside consent, unreviewed high-risk changes, or complexity exceeding observed benefit.

## 10. Integration and change control

- First proposed repository file: `docs/governance/adaptive-multi-agent-engineering.md`.
- Keep CT-WCOS v1.1 and Execution Standard 1.0 unchanged for this first adoption unless an independently justified, separately approved gap requires a minimal amendment.
- Do not edit `AGENTS.md` / `CLAUDE.md` while existing Draft PR #110 owns their stale CT-WCOS status references; prepare a minimal reference addition only after reconciling PR #110 and obtaining authorization for that edit.
- CornerMemory and CornerRouterWay remain parallel specialized tracks with stable planned interfaces; no runtime coupling required for AMAE v0.1.
- Scope of first proposed change is documentation/contract only. Implementing automatic agent or model routing requires a distinct scoped change and tests.
- Existing product/client repos require explicit separate adoption, their own security checks and release approvals.

## 11. Source and verification ledger

**Repository read-only evidence inspected 2026-11-08:** `Conquereleven/cornertech-ai` `main` at reported commit `7e43d403c50c5406fecf6b23fb4b8e497ae2aaaf`: Execution Standard 1.0; CT-WCOS v1.1; root AGENTS.md; `src/core/agents/AgentOrchestrator.js`, `AgentRegistry.js`, `src/core/memory/AgentMemoryService.js`. Existing agent components belong to the CornerOps implementation surface and do not prove a cross-tenant enterprise orchestrator.

**PR state:** Draft PR #110 open, head `7730151e6c0c744cb0c7165ac11226f1c44a0d2f`, corrects stale CT-WCOS v1.1 adoption wording. Previously adopted v1.1 via PR #109. Do not duplicate its change or treat draft state as adoption.

**Linear:** CTAI-15 in progress (M1 bootstrap, M2 dependency not presumed); CTAI-19 in progress (OpenCode/IFM checks; scope and limitations must be preserved). Pilot evidence and permission status are to be confirmed on the executing machine before further work.

**Unknowns / validation before rollout:** current M1/M2 local tool readiness, exact task authorization in each target repo, capability benchmarks across agents, cost/provider policies, chosen place for the registry, and whether docs added to repo affect integrity baselines. All remain unverified until checked.

**Decision status:** This file is a draft for Founder review. No CLI agents ran tests for this document; no independent review or local repo commit has been performed.