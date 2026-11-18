# tanpura-test

A [Songbird](https://tivra.com) project.

| | |
|---|---|
| Tempo | 130 BPM |
| Meter | 4/4 |
| Tracks | 8 |
| Clips | 10 |
| Plugins | 17 |
| Automation lanes | 3 |

## Tracks

- drone + drums
- midi
- midi [dub]
- Hall
- Plate
- Delay
- Color
- Audio

## Layout

- `bird/` — one generated `.bird` per arrangement: its sections, tracks and clips as readable notation. Rewritten on every save; edits belong in the app.
- `entities/` — content keyed by stable id (clips, plugins, automation, channels). Each file stays whole until it grows large, then transparently shards into `entities/<type>/NN.json` so merges stay size-independent.
- `spaces/` — projections that place entities (arrangement rows, mixer bus) plus per-user workspaces under `spaces/users/<id>.json` (open tabs, active tab, playback scope).
- `state/` — global project state (transport, settings, sections, …).
- `samples/` & `visuals/` — media payloads, stored in R2 (see `manifest.json`).
