# Release Notes

## v1.1.30
GH#1143 — remove 2 `default_from_previous` declarations. K-073 revoked the key, and the consumer wave has since bound every slot that carried it, so the fallback can no longer fire: the declaration was inert.

Measured before deleting rather than after: each of the 41 slots across the catalogue was resolved against **every** invocation, not just its carrier's own workflow, and all 41 were bound by every consumer. Nothing here changes behaviour — the fallback had no path to execution.

Removed: `messaging-comparison-matrix.competitor_audit`, `threat-assessment-prompt.campaign_tracking`.

## v1.1.29
GH#1100 retrospective repair — `from_step` where `from_input` was needed.

`segment-audience`'s slot is labelled **"Product or Campaign"** and was bound to Threat Assessment, so the audience segmentation was performed against a threat assessment rather than a product. No step in a competitor-monitoring flow produces a product description, so no binding to any step could have been correct. A new required `product_or_campaign` input now carries it.

**This flow now requires an input it did not require before.** Previously the user supplied nothing and the segmentation ran against a threat assessment. The old behaviour was not "fewer inputs" — it was the wrong value, silently.

This is the third consumer of `segment-audience` to have guessed at this slot, and the three guesses differed. The slot cannot declare that it takes a workflow input rather than a step output, which is the defect behind all three.

## v1.1.28
GH#1100 consumer wave (batch 3) — declare the data flow this workflow was resolving positionally.

Each stage below now receives its input through a declared `bindings:` entry instead of `default_from_previous`, which K-073 revoked. **The value is unchanged**: every binding names the step that immediately precedes it, which is exactly what the positional default resolved to. What changes is that the dependency is stated rather than inferred from position, so a reorder can no longer silently feed a stage the wrong artefact.

Bindings added:
  `segment-audience` ← `from_step: "Threat Assessment"` (step 5)

Dependency pins moved to the published versions that declare these slots:
  `audience-segmentation` 1.0.1 → 1.0.2
  `polish-language` 1.0.6 → 1.0.7
  `segment-audience` 1.0.5 → 1.0.6

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
