# Submission manifest

Generated from [snaplog](https://github.com/corleroux/snaplog) at `42951b3755ca9dbd73d7ad32c75880f09bc7672d`.

- Branch: `staging`
- Date: 2026-10-31T07:43:30+02:00
- Baseline: [hackathon-baseline](https://github.com/corleroux/snaplog/releases/tag/hackathon-baseline)
- Previous source commit: `62e0531b8a5d57ad0f78386aa5f6b52e4b470066`
- Incremental patch: `0006-62e0531-to-42951b3.patch`

## Baseline files modified since previous submission update

.gitignore
src/features/scans/api/createScanSession.ts
supabase/.sb.env.example

## Files added since baseline (copied verbatim to `new-files/`)

.opencode/agents/architect.md
.opencode/agents/builder.md
.opencode/agents/design-reviewer.md
.opencode/agents/inference.md
.opencode/agents/reviewer.md
.opencode/agents/tester.md
.opencode/opencode.jsonc
Event Details.md
docs/PRD.md
docs/plans/FR-MOD-01-provider-interface.md
docs/plans/FR-MOD-02a-muse-spark-provider.md
docs/plans/FR-MOD-02b-spark-open-modal.md
docs/plans/FR-MOD-04-benchmark-runner.md
docs/plans/FR-MOD-04-eval-set.md
docs/plans/FR-SCH-01-schema-registry.md
docs/plans/FR-SCH-03-garment-schema.md
docs/plans/FR-SCH-05-EXT-06-schema-review-ui.md
docs/plans/FR-VID-video-pipeline.md
docs/plans/README.md
docs/plans/SUB-01-submission-repo.md
docs/plans/SUB-02-demo-writeup-submission.md
modal/README.md
modal/sam_parser.py
modal/sam_segment.js
modal/test_sam_parser.py
modal/video_pipeline.py
scripts/build-submission.sh
src/features/video/api/processVideo.ts
src/lib/upload/__tests__/videoUpload.test.ts
src/lib/upload/videoUpload.ts
supabase/functions/_shared/catalogueSchemaRegistry.ts
supabase/functions/_shared/providers/extractionNormaliser.ts
supabase/functions/_shared/providers/extractionPrompt.ts
supabase/functions/_shared/providers/geminiProvider.ts
supabase/functions/_shared/providers/getProvider.ts
supabase/functions/_shared/providers/museSparkProvider.ts
supabase/functions/_shared/providers/types.ts
supabase/functions/_tests/catalogueSchemaRegistry.test.ts
supabase/functions/_tests/commit-reviewed-catalogue-item.test.ts
supabase/functions/_tests/extract-catalogue-item.test.ts
supabase/functions/_tests/extract-isolated-item.test.ts
supabase/functions/_tests/fixtures/gemini/fabric-product-tag.json
supabase/functions/_tests/fixtures/gemini/vendor-card.json
supabase/functions/_tests/fixtures/muse-spark/fabric-product-tag.json
supabase/functions/_tests/fixtures/muse-spark/vendor-card.json
supabase/functions/_tests/fixtures/sam/sam-stream.json
supabase/functions/_tests/geminiProvider.golden.test.ts
supabase/functions/_tests/getProvider.test.ts
supabase/functions/_tests/museSparkProvider.golden.test.ts
supabase/functions/_tests/process-video-document.test.ts
supabase/functions/commit-reviewed-catalogue-item/index.ts
supabase/functions/extract-catalogue-item/index.ts
supabase/functions/extract-isolated-item/index.ts
supabase/functions/process-video-document/index.ts
supabase/migrations/083_catalogue_types.sql
supabase/migrations/084_scan_sessions_run_fields.sql
supabase/migrations/085_garment_schema_and_catalogue_items.sql
supabase/migrations/086_video_jobs.sql
