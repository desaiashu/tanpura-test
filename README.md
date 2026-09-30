# live-set-2026

A [Songbird](https://tivra.com) project.

| | |
|---|---|
| Tempo | 128 BPM |
| Meter | 4/4 |
| Tracks | 64 |
| Clips | 194 |
| Plugins | 99 |
| Automation lanes | 0 |

## Tracks

- piano
- polybrute -m
- sub37
- nord
- -
- kick
- heartbeat
- kit
- sampler
- -
- mic/line
- mic/line
- mic/line
- mic/line
- surge
- stage73
- prophet
- aug voices
- infinite crate
- 20-Audio
- Samples
- Rec 1 - Bass
- Rec 2 - Kick
- Rec 3 - Mel
- Rec 4 - Harm
- Rec 5 - Drum
- Rec 6 - Drum
- Rec 7 - Drum
- Rec 8 - Misc
- Rec 9 - Misc
- MIDI
- SOUND DESIGN
- Record
- utils
- sidechain
- resampling
- reference
- reference
- bass
- kick drum
- melody
- harm
- drums
- drums
- hidrm
- hidrm
- cntr
- pad
- tnsn
- emtn
- midi
- sidechain
- Audio
- MIDI
- A-HALL 3-5s
- B-PLATE 1s
- C-CATH 10s
- D-OFF TMP DEL
- E-SPREAD DEL
- F-TAPE
- G-SATURATION
- H-WIDE
- I-QUAD L
- J-QUAD R

## Layout

- `live-set-2026.bird` — arrangement & musical intent, human-readable.
- `entities/` — content keyed by stable id (clips, plugins, automation, channels). Each file stays whole until it grows large, then transparently shards into `entities/<type>/NN.json` so merges stay size-independent.
- `spaces/` — projections that place entities (arrangement rows, mixer bus) plus per-user workspaces under `spaces/users/<id>.json` (open tabs, active tab, playback scope).
- `state/` — global project state (transport, settings, sections, …).
- `samples/` & `visuals/` — media payloads, stored in R2 (see `manifest.json`).
