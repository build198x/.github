# Build198x

The build-tools pipeline for the 198x family — everything between authored source and a runnable artifact that isn't assembly or emulation.

Three bands: asset conversion (graphics → native sprite/bitplane formats, audio → SID/AY/samples), data packing (crunchers, level/tilemap packers), and media mastering (disk and tape images, bootable media — ADF, D64, TAP, …). It meets [Asm198x](https://github.com/asm198x) at the program-framing handoff: Asm198x emits the program, Build198x masters it onto media.

## Status — active

Build198x is active. The flagship workspace contains the current build-tools implementation, including the shared media capability layer and image conversion work. The wider tool roster remains demand-gated per tool.

Inherited rules: native output only (never a bespoke format), every tool validated against a real reference where one exists, and a membership test that keeps the scope from sprawling.

## Repositories

- **[build198x](https://github.com/build198x/build198x)** — active build-tools workspace.
- **[docs](https://github.com/build198x/docs)** — design notes, and user documentation in time.

## Part of the 198x family

A sibling project to retro-computing curriculum, emulator, assembler, media-player, and cataloguing work that share a hardware-reference layer.
