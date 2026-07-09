# Build198x — org container

This folder is the local mirror of the **`build198x` GitHub org**. It is a
*container*, not a git repo: each subfolder is its own independent repo with its
own history and remote (the same pattern as `Code198x/`, `Asm198x/`, `Cat198x/`,
and `Forge198x/`). The umbrella `198x/` repo gitignores this folder; commit
inside the specific subfolder, never here.

Build198x is the 198x family's **build-tools pipeline** — asset conversion, data
packing, and media mastering: everything between authored source/assets and a
runnable artifact that is neither assembly (Asm198x) nor emulation (Emu198x). See
the umbrella context at [`../CLAUDE.md`](../CLAUDE.md) and the binding decision at
[`../decisions/build198x-build-tools.md`](../decisions/build198x-build-tools.md).

**Status: active as of 2026-06-11.** The demand gate opened on curriculum
production's need for image conversion (see
`build198x/decisions/demand-gate-opening.md`); wave 1 (the `mediaspec` capability
spec + image→native converter) is merged and active. The wider roster stays demand-gated per
tool.

## Repos in this org

| Folder | GitHub repo | Role |
|--------|-------------|------|
| [`build198x/`](build198x/) | `build198x/build198x` | **Flagship.** The build-tools workspace (active with wave-1 image converter). |
| [`.github/`](.github/) | `build198x/.github` | Org profile (`profile/README.md`) and shared community-health files. |
| [`docs/`](docs/) | `build198x/docs` | Design notes; user docs in time. |

## Working here

- **Commit in the right subfolder.** Each repo is independent; `git status` from
  the container shows nothing (it isn't a repo).
- **The membership test** (guardrail against a junk drawer): a tool belongs here
  only if it *converts, packs, or masters build inputs into machine-ready data or
  media*. Assembly → Asm198x; cataloguing existing collections → Cat198x;
  emulation → Emu198x; rendering media → Play198x.
- **Native output only** — Build198x masters to *native* containers (`.prg`,
  `.sna`, `.tap`, hunk, ADF, …), never a bespoke format, and meets Asm198x at the
  program-framing handoff (Asm198x's
  [`../Asm198x/asm198x/decisions/assemble-io-model.md`](../Asm198x/asm198x/decisions/assemble-io-model.md)).
- **Cross-project decisions** live in the umbrella [`../decisions/`](../decisions/);
  Build198x-only decisions live in `build198x/decisions/` once it starts.
