# NPU Model Optimization Competition workspace

Private working repository for the MOA Workshop at MICRO 2026 competition.

## Contents

- `baseline/` — complete competition baseline source, vendored from
  <https://github.com/HoseongLee/furiosa-opt-gemma4-12B> at commit
  `4bf1bac714d8bb9e3b8639e450a0c69d5aee93ba`.
- `official-site-snapshot/` — snapshot of the official competition website from
  <https://github.com/micro2026-moa/micro2026-moa.github.io> at commit
  `00d6217de3701e6a6eb59780ca2f2ddc5c6a47f1`.
- `YEU_CAU_CUOC_THI.md` — Vietnamese requirements dossier.
- `RESOURCE_LINKS.md` — verified official resource links.
- `ARENA_ACCESS_CHECK.md` — read-only Arena access verification.

The upstream repositories are vendored as ordinary directories so that one normal clone
contains all source files and future competition changes can be committed here directly.

## Clone on another operating system

```sh
git clone <repository-url>
cd npu-model-optimization-competition
git status
```

No Git submodule initialization is required.

## Safety

Local credentials, `.env` files, model checkpoints, generated safetensors fixtures,
build output, schedules, and logs are excluded from Git. Arena authentication remains in
the local credential store and must be configured separately on each operating system.

