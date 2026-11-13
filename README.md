# adithya-recording

A [Songbird](https://tivra.com) project.

| | |
|---|---|
| Tempo | 130 BPM |
| Meter | 4/4 |
| Tracks | 12 |
| Clips | 48 |
| Plugins | 17 |
| Automation lanes | 0 |

## Tracks

- 43 Neve 1
- Hall
- Plate
- Delay
- Color
- high scream
- 2nd high
- take 3
- lower scream
- Audio
- mids scream
- choir_7th_Feb_25

## Layout

- `adithya-recording.bird` — arrangement & musical intent, human-readable.
- `entities/` — content keyed by stable id (clips, plugins, automation, channels). Each file stays whole until it grows large, then transparently shards into `entities/<type>/NN.json` so merges stay size-independent.
- `spaces/` — projections that place entities (arrangement rows, mixer bus) plus per-user workspaces under `spaces/users/<id>.json` (open tabs, active tab, playback scope).
- `state/` — global project state (transport, settings, sections, …).
- `samples/` & `visuals/` — media payloads, stored in R2 (see `manifest.json`).
