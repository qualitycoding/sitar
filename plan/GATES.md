
## G-003 — split learning stores (v3.9)

Lessons and knowledge are pushed to **separate** stores: the `Lessons`
repository and the `knowledge` repository. G-003 requests the destinations at
plan close; **do-not-push** either store until human sign-off; the documented
bundle fallback applies when sign-off is withheld. Store publication never
holds up the repository amendment's completion record.

## G-LISTEN — blind realism listening (D-981)

- **Trigger step:** S-LISTEN (after implementation/reviews, before S-RETRO).
- **Comparison:** realism — deterministic offline renderer output vs at
  least 12 matched redistribution-compatible real sitar notes/phrases
  (low/high register, meend, jawari buzz, chikari/jhala, sympathetic
  resonance).
- **Prerequisite:** deterministic JUCE-free offline renderer (text phrase/
  event file, sample rate, seed, raga/tuning, parameter state → PCM WAV);
  CLI and event schema frozen before listening. Currently missing.
- **Frozen settings:** 12 onset pairs, `--window start`, 1.0 s clips, common
  RMS −23 dBFS (pre-match levels retained), 10 ms fades, 44.1 kHz PCM-24;
  pass = ≤ 8/12 AND no unresolved qualitative finding; max three rounds;
  base seed 20261104, rounds 2/3 add 1000/2000; p-value reported exactly;
  general mechanisms only.
- **Questions:** which side is the recorded sitar; pluck attack, jawari
  buzz, pitch/meend, sympathetic bloom, chikari/jhala rhythm, decay, stereo,
  dynamics; synthetic/clean/unstable/wrong-pitch findings by demo/time.
- **Allowed responses:** `proceed` (→ S-RETRO, then S-KNOW/G-003) |
  `iterate: <notes>` (general mechanism change; rerun affected tests; new
  seed) | `proceed-with-rescope: <text>` (narrow claim) | `stop`.
- **Status:** round-001 blocked — renderer (P-4) and references (P-5)
  missing (listening/G-LISTEN/round-001/result.json).
