<p align="center">
  <img src="./chronofield-banner.png" alt="ChronoField — exact video and storage compression" width="100%">
</p>

<h1 align="center">ChronoField</h1>

<p align="center">
  <strong>A new exact-video infrastructure stack: 225 AV1 size wins, simultaneous Full-HD size and speed gains, and another 83.65% removed across exact related renditions.</strong>
</p>

<p align="center">
  <a href="./ChronoField-safe-investor-deck.pdf"><strong>Open the 12-slide investor deck →</strong></a>
</p>

---

## Breakthrough operating points

ChronoField does not force one compromise between speed and compression depth:

| Mode | Measured result |
| --- | --- |
| **Ultra Fast** | Up to **45.63x faster encoding** than AV1 on the same exact Full-HD frames, with **37.87% fewer bytes** |
| **Fast** | **41.37% fewer bytes**, **8.42x faster encode** and **4.98x faster decode** across three real 1080p sources |
| **Archive** | Up to **55.25% fewer bytes** than the measured AV1 lossless baseline |
| **CFT + CFMS** | A complete 20-rendition compact catalog required **7.38 MB instead of 45.14 MB** after individual CFT compression: another **83.65% reduction** |
| **Full catalog economics** | **34.85× smaller than raw RGB**, exact 20/20, **261 aggregate decode fps**, and all 18 derived renditions added **zero object payload** |

Every promoted result reconstructs the original RGB frames exactly.

## Current proof

ChronoField is a working native exact-video codec and storage system.

The machine-readable result archive contains **225 recorded CFT-versus-AV1 size comparisons: 225 wins, no ties and no losses** across 62 result files and 33 benchmark suites.

In the retained CFT11 three-source Full-HD aggregate:

| Metric | Versus strict-lossless AV1 `cpu-used=4` |
| --- | ---: |
| Compressed bytes | **41.37% fewer** |
| Encode speed | **8.42× faster** |
| Decode speed | **4.98× faster** |
| Reconstruction | **Exact RGB SHA-256** |

All three real 1080p sources produced fewer bytes than both measured AV1 baselines. Peak completed Full-HD operating points reach **55.25% fewer bytes** and **29.39× faster encoding** than the measured AV1 baseline.

The current production release is **CFT11 0.28.0** with native decoder v8. Its
lossless member and collection wire formats remain unchanged, the retained
artifacts remain byte-for-byte stable, and its release gate passes **529
tests**.

The current CFMS family-storage gate uses two real source excerpts and 20 exact
related renditions in several deterministic production variants. Independent
CFT11 compact files required **45.14 MB**; the complete CFMS catalog—including
manifests and index—required **7.38 MB**, an additional **83.65% reduction**
after individual compression. All 20 outputs reconstructed exactly, aggregate
compact decode measured **261 fps**, and the full CFT + CFMS project regression
passed **598/598 tests**.

This CFMS result targets server-side rendition families created through known
production transformations—such as ABR ladders, previews, crops and version
variants. It is not presented as a universal ratio for arbitrary independent
third-party re-encodes.

> These measurements were collected locally on a Lenovo consumer laptop with
> an **AMD Ryzen 7 H 255 (8 cores / 16 threads), integrated Radeon 780M and
> 16 GB of system memory**—not on server-class hardware. Every compared codec
> used the same host and source frames. Exact RGB output is verified, and the
> benchmark is packaged for controlled third-party reproduction.

## Competitive position

Traditional lossless codecs preserve the source but do not demonstrate
ChronoField's measured Full-HD combination of density and speed. The most
relevant published neural exact-video competitor we found, NeuralLVC, reports
approximately **0.06 fps** on CIF video using an NVIDIA GH200. Fast neural
systems such as Microsoft DCVC optimize lossy rate-distortion, while
generative systems such as ByteDance CascadeV do not reconstruct the original
pixels exactly.

Our review found no public codec report demonstrating the same combination of
**exact RGB reconstruction, fewer Full-HD bytes than lossless AV1, faster
encode, faster decode, and a second exact family-storage layer that removes
another 83.65% across a measured 20-rendition production family**.

[Read the non-confidential competitive note →](./COMPETITIVE_POSITION.md)

## Why it matters

Lossless video is expensive to keep and move. Better compression can reduce infrastructure cost in:

- media archives and production pipelines;
- exact-source and mezzanine storage;
- AI and computer-vision datasets;
- scientific, medical, and regulated workflows where reconstruction must be exact.

## Next milestone

The immediate objective is independent reproduction on third-party hardware
and independently selected content, followed by server and GPU optimization
and narrow design-partner deployments. No unmeasured server-speed multiplier
is included in the results above.

## Non-confidential materials

- [Investor deck — 12 slides](./ChronoField-safe-investor-deck.pdf)
- [Competitive position — exact, neural and generative codecs](./COMPETITIVE_POSITION.md)

## Disclosure boundary

This repository intentionally contains **no source code, binaries, formulas, dictionaries, bitstream grammar, benchmark corpus, internal architecture, or protected implementation mechanics**.

## Contact

**Absamad Manturov — Founder**

[Email](mailto:absamad.manturov@gmail.com) · [GitHub](https://github.com/Absamad-dew) · [Telegram](https://t.me/Absamad_m)

---

<sub>All rights reserved. Publication grants no license to the underlying technology or these materials.</sub>
