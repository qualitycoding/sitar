# GATE-G-LISTEN — sitar realism (blind listening)

**Status:** BLOCKED — offline renderer and realism references missing
(round-001 not scored).
**Branch:** `impl/listening-validation` (base `main` @ 1aa2730ff44023ebe8ab78aeb14a6780238f001a).
**Decision:** D-981 (plan/DECISIONS.md). **Frozen seed:** 20261104 (rounds +1000/+2000).

## Test type
Realism (renderer output vs real sitar performances). The 19-test DSP suite
(T001..T019, 19/19 pass on 2026-11-03) establishes DSP properties, not
realism, and does not satisfy this gate.

## Renderer prerequisite (blocking)
No JUCE-free offline renderer exists on `main`. Before any scored round,
add a deterministic renderer that accepts a text phrase/event file, sample
rate, seed, raga/tuning and parameter state, and writes PCM WAV without
host interaction; freeze its CLI and event schema before listening.

## Frozen settings
12 matched onset pairs, `--window start`, 1.0 s clips, common RMS −23 dBFS,
10 ms fades, 44.1 kHz PCM-24 WAV; pass = ≤ 8/12 correct AND no unresolved
qualitative finding; max three rounds; a separately identified
`--window middle` sustained set is diagnostic only. Builder/scorer vendored
from qualitycoding/skills @ 7915c7b7e0cecbee5116e72a4cf5699383df5983
(sha256 3c4f75854e2a…d6824c7 / f2d9ea5c76a1…e49defa).

## Questions for the human listener
1. Which side is the recorded sitar (per pair)?
2. Per demo: convincing pluck attack, jawari buzz, pitch/meend behaviour,
   sympathetic bloom, chikari/jhala rhythm, decay, stereo character,
   dynamics? Identify any synthetic, overly clean, unstable, or wrongly
   pitched passage by demo/time.

## Allowed responses
`proceed` → close G-LISTEN, resume **S-RETRO**, then S-KNOW/G-003.
`iterate: <notes>` → general KS/jawari/tarab/meend/renderer mechanism change;
rerun all affected tests; new seed/round.
`proceed-with-rescope: <text>` → narrow the realism/technique claim before
S-RETRO.
`stop` → halt at G-LISTEN with S-RETRO pending.

## Current state
- Round-001 record: `listening/G-LISTEN/round-001/result.json`
  (status `blocked`; P-4 renderer, P-5 references missing).
