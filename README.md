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
