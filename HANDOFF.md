# Project handoff

## Objective

Prepare for and compete in the NPU Model Optimization Competition at the MOA Workshop,
MICRO 2026. Stage 1 optimizes three Gemma-4-12B-it kernels for FuriosaAI RNGD; Stage 2 is
end-to-end model optimization.

## Current state

- The private working repository contains the complete baseline as ordinary files, not a
  Git submodule.
- Official baseline provenance:
  `HoseongLee/furiosa-opt-gemma4-12B@4bf1bac714d8bb9e3b8639e450a0c69d5aee93ba`.
- Official site snapshot provenance:
  `micro2026-moa/micro2026-moa.github.io@00d6217de3701e6a6eb59780ca2f2ddc5c6a47f1`.
- Registration is confirmed.
- FuriosaAI Arena access is confirmed for the registered GitHub account.
- No Arena job has been submitted yet.
- Submission format, submission quota, final Stage 1 score formula, and most Stage 2
  benchmark details remain TBD as of the last source check.

## Key files

- `YEU_CAU_CUOC_THI.md`: complete Vietnamese competition requirements and open TBDs.
- `RESOURCE_LINKS.md`: verified official technical resources.
- `ARENA_ACCESS_CHECK.md`: read-only Arena UI and access findings.
- `baseline/README.md`: official competition guide.
- `baseline/OPTIMIZATION.md`: official Stage 1 workflow.
- `baseline/tests/test_kernels.rs`: grading truth for the three public kernel tests.

## Next intended work

1. Clone this repository on supported Ubuntu.
2. Install the pinned Rust/Furiosa toolchain from `baseline/README.md`.
3. Generate the public fixture if it is not present.
4. Configure `furiosa-arena-cli` and run `rngd login` locally on Ubuntu.
5. Run the untouched baseline public RNGD test and preserve the output as the initial
   correctness/performance baseline.
6. Analyze schedules for each Stage 1 kernel before implementing optimizations.

## Prompt for a new Codex session

Use this exact prompt after selecting this repository:

> Read `AGENTS.md` and `HANDOFF.md` completely, then inspect the repository status. Treat
> `YEU_CAU_CUOC_THI.md` and `baseline/README.md` as the current competition context. Tell
> me what is already complete, verify whether the official site or baseline has changed,
> and continue from the next intended work without redoing completed setup.

