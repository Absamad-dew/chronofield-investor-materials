<p align="center">
  <img src="./chronofield-banner.png" alt="ChronoField — exact video and storage compression" width="100%">
</p>

<h1 align="center">ChronoField</h1>

<p align="center">
  <strong>Strict-lossless video compression with 225 wins in 225 recorded size comparisons against AV1.</strong>
</p>

<p align="center">
  <a href="./ChronoField-safe-investor-deck.pdf"><strong>Open the 12-slide investor deck →</strong></a>
</p>

---

## Current proof

ChronoField is a working native exact-video codec and storage system.

The machine-readable result archive contains **225 recorded CFT-versus-AV1 size comparisons: 225 wins, no ties and no losses** across 62 result files and 33 benchmark suites.

In the current CFT11 0.27.0 three-source Full-HD aggregate:

| Metric | Versus strict-lossless AV1 `cpu-used=4` |
| --- | ---: |
| Compressed bytes | **41.37% fewer** |
| Encode speed | **8.42× faster** |
| Decode speed | **4.98× faster** |
| Reconstruction | **Exact RGB SHA-256** |

All three real 1080p sources produced fewer bytes than both measured AV1 baselines. Peak completed Full-HD operating points reach **55.25% fewer bytes** and **29.39× faster encoding** than the measured AV1 baseline.

The current native release passes **512 tests** and preserves decode compatibility across member wire versions v7–v14.

> The comparison uses the same source frames and hardware for every codec, verifies exact RGB output, and is packaged for controlled third-party reproduction.

## Why it matters

Lossless video is expensive to keep and move. Better compression can reduce infrastructure cost in:

- media archives and production pipelines;
- exact-source and mezzanine storage;
- AI and computer-vision datasets;
- scientific, medical, and regulated workflows where reconstruction must be exact.

## Next milestone

The immediate objective is independent reproduction on third-party hardware and independently selected content, followed by server optimization and narrow design-partner deployments.

## Non-confidential materials

- [Investor deck — 12 slides](./ChronoField-safe-investor-deck.pdf)

## Disclosure boundary

This repository intentionally contains **no source code, binaries, formulas, dictionaries, bitstream grammar, benchmark corpus, internal architecture, or protected implementation mechanics**.

## Contact

**Absamad Manturov — Founder**

[Email](mailto:absamad.manturov@gmail.com) · [GitHub](https://github.com/Absamad-dew) · [Telegram](https://t.me/Absamad_m)

---

<sub>All rights reserved. Publication grants no license to the underlying technology or these materials.</sub>
