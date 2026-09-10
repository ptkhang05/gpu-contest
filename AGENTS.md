# Project guidance

Before planning or changing code, read these files in order:

1. `HANDOFF.md`
2. `YEU_CAU_CUOC_THI.md`
3. `baseline/README.md`
4. `baseline/OPTIMIZATION.md`

Treat `baseline/tests/test_kernels.rs` as the Stage 1 source of truth for correctness and
kernel timing. Preserve every `#[device]` function name and signature. Only assume a rule
is final when the official website or baseline confirms it; explicitly label all TBD/TBA
items and re-check upstream before competition-critical decisions.

Never commit credentials, Arena authentication, model checkpoints, generated
`.safetensors` files, build outputs, schedules, or logs. Do not submit or cancel Arena jobs
unless the user explicitly asks.

