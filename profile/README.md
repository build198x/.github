# Build198x

The build-tools pipeline for the 198x family — everything between authored source and a runnable artifact that isn't assembly or emulation.

Three bands: asset conversion (graphics → native sprite/bitplane formats, audio → SID/AY/samples), data packing (crunchers, level/tilemap packers), and media mastering (disk and tape images, bootable media — ADF, D64, TAP, …). It meets [Asm198x](https://github.com/asm198x) at the program-framing handoff: Asm198x emits the program, Build198x masters it onto media.

## Status — decided, not yet started

Not built yet, and deliberately so. Build198x is demand-gated: the family's near-term work ships Asm198x program framings, not Build198x volumes, so nothing waits on it. The repos exist to hold the work; the work waits for a concrete need.

Inherited rules: native output only (never a bespoke format), every tool validated against a real reference where one exists, and a membership test that keeps the scope from sprawling.

## Repositories

- **[build198x](https://github.com/build198x/build198x)** — the build-tools workspace (placeholder for now).
- **[docs](https://github.com/build198x/docs)** — design notes, and user documentation in time.

## Part of the 198x family

A sibling project to retro-computing curriculum, emulator, assembler, media-player, and cataloguing work that share a hardware-reference layer.
