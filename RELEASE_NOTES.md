# Release Notes

## v1.1.27
GH#863 Wave 1 — fix the K-045 intent/output mismatch: the bundle shipped the `messaging-comparison-matrix`, `threat-assessment-prompt`, and `monitoring-report-writer` prompts (the monitoring report being the real deliverable) and the docs said to run them, but the `execution:` block never invoked any of them — so the periodic report was never produced. Restored the intended bound graph: added **Messaging Comparison Matrix**, **Threat Assessment**, and **Monitoring Report Writer** execution steps (each with a backing skill so it is `from_step`-addressable), ordered `messaging-analysis → messaging-comparison → market-signal-detection → threat-assessment → audience-segmentation → monitoring-report`, and rewired every cross-step input to an explicit `from_step` binding (`{{step.context.*}}`) instead of positional `{{steps.previous.output}}` / `{{steps.<Title>.output}}` refs. The monitoring report is now the last content step and receives the messaging matrix, threat assessment, and market signals. Also repinned `polish-language` 1.0.1→1.0.6 (the version exposing the bindable `source` slot) and bound `language-polish`'s `source` ← the Monitoring Report Writer output, so the `output_step` polishes the actual report rather than its positional previous. No new required inputs.

## v1.1.26
GH#845 — republish with American English (en-US) content, completing the source-only GH#805 flip that never reached the Hub. Copy only — no functional or behaviour change.

## v1.1.25
GH#745 — declare per-step `output: {name, type}` on every execution step (messaging_analysis/text, market_signals/text, audience_segments/list, polished_report/text). Lights up the #744 rich flow-map. Content-only; no bindings or logic changes.

## v1.1.24
GH#645 Row 3b — migrate to K-037 dep-referenced schema. Strip 6 inline shared-content files and declare 6 hub-shared deps (UUID id + slug name + version + checksum from `gen-dep-checksums.mjs`). Closes pre-Step-3 inline-vendoring for this bundle.

## v1.1.23
Wave 2: re-signed with canonical engine signing pipeline.

## v1.1.22
Tags migrated inline into manifest (GH#586). tags.yaml retired.

## v1.1.21
Bundle re-signed with canonical engine signing pipeline (Wave 2 migration).

## v1.1.20
Signature fix — RELEASE_NOTES.md now included in integrity checksum.

## v1.1.19
Initial catalog release with full structural and content-quality validation. All scanner checks pass.
