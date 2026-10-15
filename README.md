# valhalla-lite

A tiny repository-local harness for coding agents: product, engineering, and testing context, discovered through existing AGENTS.md instructions.

## Onboard a repository

Tell your coding agent:

> Onboard Valhalla Lite from https://github.com/zakkriel/valhalla-lite into my repository. Obtain the source and use its onboarding skill. Stop after onboarding.

Specify the target path if the agent is not already in it. The agent obtains a separate source checkout and reads [the self-contained onboarding skill](skills/valhalla-onboard/SKILL.md). No global installation, dependencies, server, or database are needed for the harness.

Onboarding reads the app and existing instructions, runs relevant baseline checks, creates three small Markdown context files under harness/, and appends a discovery/use section to AGENTS.md while preserving existing instructions. It also creates harness/read-log.md for honest full/partial file reads and task-relevant purposes. Existing harness content and unrelated user edits must be preserved and reconciled.

## Use it

Start a fresh coding conversation in the target and make an ordinary bounded behavior-change request. AGENTS.md directs the agent to read and use the context, establish acceptance, implement the change, execute discriminating checks, and persist results and gaps. Read-log claims must be cross-checked against actual recorded reads; a log alone is not proof.

## POC acceptance

Source acquisition → onboarding → fresh conversation → discovery → change → executed checks → saved result. Preserve original instructions, input data, and unrelated changes. Where safe and useful, an isolated deliberately wrong implementation should fail the relevant check. A public test app may be synthetic; label that limitation rather than claiming production adoption.

This is an agent-operated POC, not a packaged executable installer or automatic agent bootstrap. Keep the context plain and the workflow small. Do not publish sensitive traces, private external paths, or credentials in a public target.

Read-log privacy is mandatory: the skill supplies an explicit clause that onboarding must copy unchanged into AGENTS.md. Public harness entries use repository-relative paths or neutral redacted external identifiers; exact external mappings stay in private session evidence outside the target. The [test repository proof](https://github.com/zakkriel/testing-Repo-Valhalla/blob/main/PROOF.md) preserves the original privacy failure and a fresh follow-up that logged safely without publication-time path substitution.

## Product-only iteration

To install the Product harness, ask your coding agent:

> Onboard the Product harness from https://github.com/zakkriel/valhalla-lite into my repository using skills/valhalla-product/SKILL.md. Inspect the product, record material questions, and stop pending validation. Do not implement app features.

The [Product skill](skills/valhalla-product/SKILL.md) creates one compact product understanding and a small validation handoff. It separates code observations from intended behavior, asks only material questions, updates understanding from answers, and requires confirmation before reuse. A disclosed test-owner fixture can validate a synthetic product; it never substitutes for a real owner's confirmation.

After confirmation, a fresh task receives an ordinary feature-planning request. It discovers product context through AGENTS.md and produces a grounded user outcome and observable acceptance conditions before coding. This iteration stops at the brief; it does not add Engineering/Testing harnesses or implement an app feature. Evaluate the brief against confirmed facts and source evidence, not read counts.

[Product-only proof and limits](https://github.com/zakkriel/testing-Repo-Valhalla/blob/main/PRODUCT-PROOF.md): an explicitly synthetic owner role answered material questions and separately confirmed updated understanding; a fresh task produced a grounded discount brief, and independent review evaluated its content and examples. No discount code or Engineering/Testing harness expansion was made. For acquisition evidence, use a new source checkout and cite the exact revision where the skill is tracked.

Documentation: [mechanism, responsibilities and correction](docs/README.md).
