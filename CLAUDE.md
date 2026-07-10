# Build198x — org container

This folder is the org container for the **`build198x` GitHub organisation**. It is not a Git repo; each child folder is an independent repo with its own remote. Commit inside the repo that owns the file.

Build198x is the 198x family's **build-tools pipeline** — asset conversion, data
packing, and media mastering: everything between authored source/assets and a
runnable artifact that is neither assembly (Asm198x) nor emulation (Emu198x). See
the umbrella context at [`../CLAUDE.md`](../CLAUDE.md) and the binding decision at
[`../decisions/build198x-build-tools.md`](../decisions/build198x-build-tools.md).

**Status: active.** The flagship workspace contains the current build-tools
implementation, including the shared media capability layer and image conversion
work. The wider tool roster remains demand-gated per tool.

## Repos in this org

| Folder | GitHub repo | Role |
|--------|-------------|------|
| [`build198x/`](build198x/) | `build198x/build198x` | **Flagship.** The build-tools workspace (active with wave-1 image converter). |
| [`.github/`](.github/) | `build198x/.github` | Org profile (`profile/README.md`) and shared community-health files. |
| [`docs/`](docs/) | `build198x/docs` | Design notes; user docs in time. |
| [`build198x.github.io/`](build198x.github.io/) | `build198x/build198x.github.io` | Public site (Astro, GitHub Pages via Actions). House style mirrors `emu198x.github.io`. |

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
