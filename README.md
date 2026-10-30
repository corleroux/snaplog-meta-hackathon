# Snaplog — Meta × Cerebral Valley Hackathon Submission

**Track:** Startup · **Theme:** "Build for Your World." · **Tagline:** "Snap it. Catalogued."

This repository contains only the event-week work for [Snaplog](https://github.com/corleroux/snaplog). The pre-existing codebase is at [`corleroux/snaplog@hackathon-baseline`](https://github.com/corleroux/snaplog/releases/tag/hackathon-baseline).

## What existed before

A mobile-first **fabric catalogue** for fashion buyers at international trade fairs. A buyer photographs a fabric swatch and the vendor's business card or stall front; a Supabase Edge Function extracts structured fields with Gemini; the buyer reviews and commits; the catalogue is searchable. Stack: React 19 + TypeScript + Vite + Capacitor, Supabase (Postgres, Storage, Edge Functions).

## What we are building this week

| Capability | Status |
|---|---|
| Schema registry — catalogue types as config | In progress |
| Provider interface (Gemini, Muse Spark, open weights) | In progress |
| Garments as a second category, no code changes | In progress |
| Video pipeline with SAM 3.1 item isolation on Modal | In progress |
| Benchmark runner: accuracy, latency, cost | In progress |
| Schema-driven review UI | In progress |

Built with **Muse Spark Open** and Meta's model stack.

## Rebuild the demo

```bash
# 1. Clone this submission repo
git clone https://github.com/corleroux/snaplog-meta-hackathon.git
cd snaplog-meta-hackathon

# 2. Clone the pre-existing codebase at the hackathon baseline
git clone --branch hackathon-baseline https://github.com/corleroux/snaplog.git ../snaplog-hackathon
cd ../snaplog-hackathon

# 3. Apply all incremental patches in order
git apply ../snaplog-meta-hackathon/patches/*.patch

# 4. Copy new files (providers, registry, schemas, video pipeline, benchmark,
#    docs/plans, eval manifest, write-up) into place.
#    Use `cp -a` so hidden directories such as .opencode/ are included.
cp -a ../snaplog-meta-hackathon/new-files/. .

# 5. Install dependencies and configure environment
pnpm install
cp .env.example .env
cp supabase/.sb.env.example supabase/.sb.env
# Fill in VITE_SUPABASE_URL / VITE_SUPABASE_ANON_KEY in .env
# Fill in edge-function secrets in supabase/.sb.env

# 6. Run the app locally
pnpm dev
```

Supabase (one shared project for staging/production until a planned split; treat all data as production):

```bash
supabase link --project-ref <project-ref>
supabase db push
supabase secrets set --env-file supabase/.sb.env --project-ref <project-ref>
supabase functions deploy --project-ref <project-ref>
```

## Model attribution

| Capability | Model | Runtime |
|---|---|---|
| Photo extraction | Muse Spark via Meta Model API | Supabase Edge Function |
| Item isolation in video | SAM 3.1 | Modal |
| Open-weights comparison | Muse Spark Open | Modal |
| Baseline (fixtures / write-up only) | Gemini | — |

Every model the demo calls at runtime is Meta.

## Submission contents

- `patches/*.patch` — incremental diffs of files modified since the baseline.
- `new-files/` — verbatim copies of files added since the baseline.
- `MANIFEST.md` — source commit, branch, date and file lists.
- `docs/plans/` — one plan per hackathon task.
- `eval/` — evaluation manifest (captures themselves are excluded from the public repo; added in FR-MOD-04).

## Submission checklist

- [x] Public repo with event work only
- [x] Baseline tag on pre-existing code
- [x] Incremental commit history
- [x] Setup instructions in README
- [x] Built with Muse Spark Open attribution
- [x] Startup track declared

## Bonus opt-ins

- [ ] Open-source release post-hackathon
- [ ] Continue building with Meta tools
- [ ] Publish benchmark write-up

---

Generated from `corleroux/snaplog`. See [`MANIFEST.md`](MANIFEST.md) for the exact source commit.
