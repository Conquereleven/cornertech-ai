# CornerTech AI · Execution Standard 1.1

Single operational standard for ordinary engineering, product and AI-assisted work after explicit repository adoption. Earlier versions remain in [Git history](https://github.com/Conquereleven/cornertech-ai/tree/db31f24032b87371e650b54a3f2ae6da5a05c4bf/docs/governance). No new permissions are granted here.

## Deliver

1. One DRI owns the user/business outcome. When scope and permission are clear, execute directly. Keep the existing task or PR; no new plan, ticket, handoff or approval just for routine work.
2. **SOLO is the default**, including ordinary feature development, UI, fixes and tests. Add a reviewer or specialist only for material risk, a required control, or a demonstrable missing capability. Preserve any mandatory independent review; never describe self-review as independent. Concurrent writers must have clear ownership.
3. Work from the relevant files and accepted design/functional contract. Deliver a working preview early for UI work. Fix root causes instead of accumulating patches. Reuse evidence when its scope, inputs and relevant behavior remain valid; never claim evidence for an untested SHA or environment.
4. Check tools and model availability when needed. Avoid redundant research, delegation and test suites. After two failed attempts for the same cause, change the approach before repeating. Record usage if readily observable; unknown usage is not an invented cost or a routine-work blocker. No unauthorized provider, spend or data transfer.

## Protect

5. Existing security, privacy, tenant isolation, customer/release and environment rules remain controlling. Reuse exact valid GO; never broaden it. Push, PR, merge, deploy, infrastructure, credentials, spend, customer data, payments and external communications retain their own applicable permissions. A merge that triggers deployment also needs deployment approval. [Permissions](../security/permissions.md) and [human approvals](../security/human-in-the-loop.md) apply; execute local checks and scripts only within applicable existing authorization.
6. Scale verification to impact. For ordinary changes, test affected behavior and meaningful negative cases; for payments, authorization, data integrity, tenant isolation, credentials, infrastructure or production risks, retain the applicable critical tests, independent review, rollback/recovery and release gates. Do not bypass CI or weaken security/integrity tests. If review is required and unavailable, hold only the affected action.
7. Block only the unsafe, unavailable or unauthorized effect. Continue independent authorized work. Use read-only evidence first where permitted; never expose client data or secrets or invent a result.

## Verify and finish

8. Use one existing record for the outcome, DRI, scope/GO, material acceptance checks, changed SHA/resources and remaining blocker. For routine work a concise change summary and test result suffice. No mandatory extra forms or per-agent receipts.
9. Distinguish **PREPARED** (ready), **EXECUTED** (change made), **VERIFIED** (acceptance checked in the stated environment), **CLOSED** (verified outcome and any required acceptance), and **BLOCKED** (specific unresolved dependency). CI, local/synthetic tests, previews, merges and reports do not prove Production acceptance. Verify real behavior at the destination when authorized. Keep proof inspectable and state limitations honestly.
10. Finish with the result, evidence and only the remaining decision or action, if any. A governance change is not adopted in a repository/agent merely because it is merged elsewhere; confirm applicable instructions in the actual working environment. Do not require a full adoption audit for every task.

## References only when relevant

- [CT-WCOS + 9D](world-class-operating-standard.md): strategic quality and foresight, not a separate task gate.
- [AMAE](adaptive-multi-agent-engineering.md): agent selection guidance; the operational rule is above.
- [Design & Storefront](design-storefront-standard.md) and [Agent Memory Governance](agent-memory-governance.md): apply relevant adopted domain requirements only. Existing stricter mandatory controls remain in force.

**One control. One evidence. One approval.**
