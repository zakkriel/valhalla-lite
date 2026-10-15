---
name: valhalla-product
description: Onboard and validate a repository's product understanding, then use it for a grounded feature brief before implementation. Use for Product-only Valhalla Lite onboarding or product planning; do not implement app features.
---

# Product harness

Goal: save accurate product understanding that a fresh coding agent can reuse to
produce an intended user outcome and observable acceptance conditions before coding.
This workflow ends at the feature brief. Add no runtime feature or Engineering/
Testing harness expansion.

## Install and understand

Obtain the requested Valhalla Lite source checkout. Read the target's existing
instructions, product context and working-tree state before editing. Preserve
existing instructions, unrelated edits and prior evidence. Reconcile an existing
product document using source evidence rather than silently replacing its facts.

Inspect relevant code, docs, examples and proportionate existing checks. Maintain
one compact `harness/product.md` covering users, problem, capabilities, key rules,
evidence links, assumptions and unanswered questions. Label current observed
behavior separately from intended behavior; code is not owner intent. Link claims
to repository paths or immutable source references. Distinguish missing coverage
from unsupported product requirements.

Ask only questions whose answers materially change the product understanding or
feature scope. Record them with answers and confirmation status in one small
`harness/product-validation.md` handoff. Update product.md from actual answers,
then obtain confirmation of that updated understanding. Never invent confirmation.
If confirmation is unavailable, leave it pending and state the specific blocker.
A synthetic test-owner role may answer only against a disclosed fixture; label
its answers and confirmation as fixture validation, never real-owner approval.

Append a short `valhalla-product` discovery section to AGENTS.md, preserving the
existing instructions. Link the product and validation documents, require reading
them before product planning, and instruct a fresh agent to establish the intended
user outcome, observable acceptance and unresolved decisions before coding. Reuse
an identical section on repeat; reconcile conflicts rather than duplicating or
overwriting. Existing read-log and privacy instructions remain in force.

Use the existing plain `harness/read-log.md`: one entry per complete read receipt,
including repeats, with path and task-relevant purpose; partial reads need their
actual extent. Complete claims require complete untruncated receipt. Cross-check
claims and read actions in both directions. Searches/checksums and internal script
file access are not complete file receipts.

Copy this privacy clause unchanged into the installed Product discovery section:

Read-log privacy: Never write a host-absolute private external path or private instruction contents into harness files, including entry purposes. Use repository-relative paths for target files. For external private reads, use a neutral identifier such as `[redacted external instruction A]`; `external:` followed by a literal private path is not redaction. Keep the exact identifier-to-path mapping only in the coding session's private work directory outside the target repository. Check each entry before appending it. Preserve auditability through that private mapping and the recorded read action.

## Reuse and evaluate

After validation, a fresh task receives an ordinary feature-planning request with
no repeated product explanation. It must discover the installed context, cite the
confirmed facts it uses, separate current capabilities from the proposed feature,
and save a compact feature brief under `harness/`. Include intended user outcome,
scope, concrete examples/acceptance and unresolved decisions; stop before coding.

Evaluate the brief against the confirmed facts and source evidence, not read counts.
Check at least the assumptions that could cause the wrong feature or acceptance.
If intended behavior is unresolved, mark it as a proposal/question rather than an
existing capability or owner decision. Retain actual evidence and limitations.
