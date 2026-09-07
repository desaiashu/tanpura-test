# tanpura-test

A [Songbird](https://tivra.com) project.

| | |
|---|---|
| Tempo | 130 BPM |
| Meter | 4/4 |
| Tracks | 9 |
| Clips | 5 |
| Plugins | 15 |
| Automation lanes | 3 |

## Tracks

- drone + drums
- midi
- midi [dub]
- Hall
- Plate
- Delay
- Color
- Palette Patterns
- Audio

## Layout

- `tanpura-test.bird` — arrangement & musical intent, human-readable.
- `entities/` — content keyed by stable id (clips, plugins, automation, channels). Each file stays whole until it grows large, then transparently shards into `entities/<type>/NN.json` so merges stay size-independent.
- `views/` — projections that place entities (arrangement rows, mixer bus). New views (palette, session) are added here without touching content.
- `state/` — global project state (transport, settings, sections, …).
- `samples/` & `visuals/` — media payloads, stored in R2 (see `manifest.json`).
