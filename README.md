# Density Over Time

A sound clip rendered as one solid object, as a study for a physical sculpture.

**[View it running →](https://yak-man.github.io/density-time-study/)**

A uniform medium of particles is pushed up the pressure gradient, so particles
crowd into compressions and leave rarefactions empty. The density pattern is
emergent rather than painted on. Each moment of the clip contributes its own
field, laid out along a time axis, so the whole recording becomes a single form:

- **Column** — vertical is time, bottom is the start. Every horizontal slice is
  the real pressure field around the sources at that moment, at real
  wavelengths; the slice is 3 m of air.
- **Sphere** — radius is time, outer is the start and the centre is the end.
  Every shell is the far-field pattern the sources threw in each direction at
  that moment.

Both are also shown as they would look laser-engraved into a glass block, and
the point clouds export as `.xyz`.

## What is physical and what is a choice

Wavelengths, source spacing, interference, loudness in dB and timing are kept
exact. Two presentational decisions are made deliberately:

- **Stroboscopic.** Every partial is frozen at the same phase, as if lit by a
  strobe, so a steady note makes a steady shape. At any honest time scale a
  440 Hz wave cycles 1,760 times in four seconds, and no print can hold that.
- **Exaggerated amplitude.** Displacement is far larger than air really moves,
  enough that particles fold into sheets.

Along the time axis particles never move. That axis is time, not space, and
shifting them along it would smear neighbouring moments together.

## Using it

Open the page and it renders a built-in synthesised test phrase — no audio file
needed. Use **Load a sound file…** to render your own; the audio is decoded in
your browser and never uploaded. The **Sphere** menu switches between open air,
a resonant shell, accretion, and the two combined.

Some URL parameters are useful: `?n=` sets the particle count (default 500000;
try `?n=60000` for a quick preview), `?spts=` the engraved point count, and
`?file=`, `?t0=`, `?t1=` load and trim a clip by URL.

**Not working here:** `?bluff=1`, `?compare=1` and `?examples=1` are comparison
grids that load specific audio from a `local-samples/` folder. Those files are
music and are not redistributed, so those three views will fail on this site.
Everything else works.

## Requirements

A browser with WebGL2. [Three.js](https://threejs.org/) r169 (MIT) loads from a
CDN, so the page needs a network connection the first time. There is no build
step and no server — the single `index.html` is the whole thing.

Rendering 500,000 particles takes a few seconds and a fair amount of memory.

## Origin

Extracted from a larger private project exploring sound as printable geometry.
This repository holds the one self-contained study.
