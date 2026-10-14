---
name: valhalla-onboard
description: Onboard a local repository with a minimal Valhalla Lite harness containing product, engineering, and testing context, preserving existing instructions. Use when asked to onboard Valhalla Lite into a target repository.
---

# Valhalla Lite onboarding

This skill performs repository-local onboarding. It needs no global installation,
dependencies, server, database, or access to the original author's workspace.

## Onboard the target

Read the target's existing instructions, current code, and working-tree state.
Identify its user outcome, relevant implementation paths, constraints, and normal
checks. Run relevant existing checks at proportionate cost and inspect one runnable
behavior when available. Record unavailable checks and uncertainty without inventing
requirements. Do not change app behavior during onboarding.

Create three concise plain Markdown files under `harness/`: product understanding,
engineering understanding, and testing understanding. Filenames can fit the target;
`product.md`, `engineering.md`, and `testing.md` are simple defaults. Ground claims
in source paths. Testing context records actual commands, outcomes, and the risks
they check, along with gaps. Existing harness content must be inspected and
reconciled rather than silently replaced. Avoid following symlinks outside the
authorized target.

Append a short discovery/use section to `AGENTS.md` preserving its existing bytes
and instructions. Create AGENTS.md if absent. Delimit only the added section with
`<!-- valhalla-lite:start -->` and `<!-- valhalla-lite:end -->`. Link to the actual
three files using relative paths. The section tells a future coding agent to:

- Read the three contexts before a behavior change; reconcile them with current code.
- Establish the requested outcome and acceptance, preserve repository constraints,
  and choose checks that distinguish the requested behavior from a wrong result.
- Execute relevant checks and persist the request, changed paths, actual outcomes,
  and remaining gaps in the harness; update stale understanding as needed.
- Append each complete file read to `harness/read-log.md` with the file path and a
  brief task-relevant purpose. Mark partial reads as `partial` with the portion
  read; never log them as `full`. A `full` claim requires receiving the complete
  contents through a recorded read action, with no output truncation. Use a plain
  log, for example `full | src/cli.mjs | locate argument parsing`. Include context
  file reads, not just code reads. Cross-check final read-log claims against actual
  read actions; report unmatched claims rather than treating a log as proof.

Log one entry per read occurrence, including repeated reads, as soon as practical
after receiving the contents. Include onboarding source/instruction reads as well
as target reads. Do not treat a checksum, search match, or a script's internal file
access as receipt of the complete contents. Before delivery, compare both ways:
every full claim has a complete read action, and every complete read action has
an entry. Record partial reads with their line range or other clear extent.
For a public target, do not expose private external paths or instruction contents:
use a clearly labeled redacted external path identifier and retain any exact
mapping in private verification evidence. Repository-relative paths are preferred.

Create `harness/read-log.md` as the plain read log alongside the three context
files. Record onboarding reads using the same honest distinction; do not backfill
unsupported claims. Read logging is a required POC behavior, not a telemetry system.

Reuse an identical discovery section on rerun. If a different existing section or
conflicting instructions require reconciliation, preserve them and surface that
conflict before changing them. Preserve unrelated dirty files. Inspect the complete
onboarding diff and verify that only the three context files, read log, and discovery section
were changed. Reapply an identical onboarding decision to verify no duplication or
overwrite. Report baseline checks, preservation, and limits, then stop onboarding.

## Separate behavior proof

A later fresh coding session receives an ordinary bounded change request. It must
discover these repository instructions, use context, edit real behavior, execute
discriminating checks, and persist evidence/gaps. Onboarding alone does not prove
that sequence. Where safe and useful, verify a deliberately wrong version fails
the relevant check in an isolated copy, leaving the working target correct.

Keep the workflow tiny. Add no framework, schema engine, automatic agent bootstrap,
or old Valhalla architecture. Respect the target's existing permissions and scope.
