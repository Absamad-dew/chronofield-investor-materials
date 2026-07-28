<p align="center">
  <img src="./chronofield-banner.png" alt="ChronoField — exact video and storage compression" width="100%">
</p>

<h1 align="center">ChronoField</h1>

<p align="center">
  <strong>Strict-lossless Full-HD video compression for storage- and compute-heavy infrastructure.</strong>
</p>

<p align="center">
  <a href="./ChronoField-safe-investor-deck.pdf"><strong>Open the 12-slide investor deck →</strong></a>
</p>

---

## Current proof

ChronoField is an early-stage codec R&D project built around exact reconstruction, materially smaller storage footprints, and practical decode performance.

| Measured profile | Compressed size vs. strict-lossless AV1 | Encode speed vs. strict-lossless AV1 |
| --- | ---: | ---: |
| **Realtime** | **48.20% fewer bytes** | **22.59× faster** |
| **Archive** | **55.25% fewer bytes** | **1.43× faster** |

The current internal benchmark covers **900 Full-HD frames from two real 1080p sources**. Six measured ChronoField profiles simultaneously beat the measured AV1 baseline on both compressed size and encode speed, with exact RGB reconstruction for every decoded frame.

The current native release passes **461/461 tests**.

> These results are internal and corpus-specific. They have not yet been independently validated and should not be interpreted as a universal performance claim.

## Why it matters

Lossless video is expensive to keep and move. Better compression can reduce infrastructure cost in:

- media archives and production pipelines;
- exact-source and mezzanine storage;
- AI and computer-vision datasets;
- scientific, medical, and regulated workflows where reconstruction must be exact.

## Next milestone

The immediate objective is controlled third-party reproduction on independently selected content and hardware, followed by a broader reproducible benchmark against established lossless codecs.

## Non-confidential materials

- [Investor deck — 12 slides](./ChronoField-safe-investor-deck.pdf)

## Disclosure boundary

This repository intentionally contains **no source code, binaries, formulas, dictionaries, bitstream grammar, benchmark corpus, internal architecture, or protected implementation mechanics**.

## Contact

**Absamad Manturov — Founder**

[Email](mailto:absamad.manturov@gmail.com) · [GitHub](https://github.com/Absamad-dew) · [Telegram](https://t.me/Absamad_m)

---

<sub>All rights reserved. Publication grants no license to the underlying technology or these materials.</sub>
