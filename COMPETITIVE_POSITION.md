# ChronoField competitive position

This is a non-confidential market note. It contains no source code, binaries,
formulas, dictionaries, bitstream grammar, corpus, internal architecture, or
protected implementation mechanics.

## The result that matters

ChronoField has produced fewer bytes than lossless AV1 in **225 of 225
recorded comparisons**. In the retained three-source Full-HD fast benchmark,
it produced **41.37% fewer bytes** while encoding **8.42x faster** and decoding
**4.98x faster** than AV1 `cpu-used=4`. Every source reconstructed to the
exact RGB SHA-256.

On one measured Full-HD source, the Ultra Fast profile produced **37.87%
fewer bytes**, encoded **45.63x faster**, and decoded **4.66x faster** than
the same strict-lossless AV1 baseline.

The separate CFMS family-storage layer then removes redundancy across related
renditions after the individual streams have already been compressed. In a
20-rendition exact family benchmark, independent CFT required **56.26 MB** and
CFMS reduced the physical footprint to **20.73 MB**—an additional **63.15%**
reduction—with exact reconstruction and **256.57 aggregate decode fps**.

## What public competitors optimize

| System | Reconstruction | Public evidence | Commercial implication |
| --- | --- | --- | --- |
| **Lossless AV1** | Exact in the audited configuration | Direct ChronoField baseline | ChronoField wins all 225 recorded size comparisons and has simultaneous Full-HD size/speed wins |
| **AV2 v1.0 lossless** | Exact lossless mode is defined in the June 2026 AOMedia specification | Published 29.81%/33.79% BD-rate gains vs AV1 are lossy PSNR-YUV/VMAF results; no public exact Full-HD lossless result was found | Newest serious standard challenger and the highest-priority direct benchmark still to run |
| **FFV1** | Exact, intra-frame | IETF-standardized preservation codec | Mature archival incumbent, not the compression frontier in the reviewed evidence |
| **H.264 / H.265 lossless** | Exact in lossless profiles | Traditional exact video baselines | Strong ecosystem, but no reviewed report reproduces ChronoField's complete Full-HD combination |
| **NeuralLVC (2026)** | Exact YUV420 video; RGB exactness reported for still images | 29.71% of raw YUV420 on nine Xiph CIF sequences; approximately 0.06 fps on NVIDIA GH200 | The most relevant published neural exact-video competitor found, but currently offline-scale |
| **VVC QP=0 in NeuralLVC** | Near-lossless, not exact in that test | 27.24% of raw YUV420 on Xiph CIF | Strong numeric rate, disqualified where byte-exact reconstruction is required |
| **Microsoft DCVC-RT** | Lossy | 125.2 fps encode / 112.8 fps decode at 1080p on NVIDIA A100; 21% bitrate saving against VTM in rate-distortion evaluation | Fast neural delivery, but not an exact-lossless substitute |
| **ByteDance CascadeV** | Generative/lossy | 1024x latent dimensionality reduction; imperfect reconstruction; almost one minute for eight 1024x1024 frames on one NVIDIA A800 | Extreme latent representation by giving up pixel identity |
| **MagicYUV / UT Video / Lagarith / HuffYUV** | Exact capture/intermediate codecs | Public positioning prioritizes recording and editing throughput | Important speed incumbents, but no reviewed report reproduces the complete ChronoField combination |
| **Motion JPEG 2000 / JPEG XL sequences** | Exact per-frame lossless coding | Mature image/archive systems with independent frame codestreams | Strong random access, but no native cross-frame redundancy |
| **ChronoField CFT + CFMS** | Exact RGB plus exact family storage | Direct Full-HD AV1 gates and a separate related-rendition storage gate | Density, practical speed, and cross-rendition economics in one stack |

## Conclusion

The reviewed competitors are strong on individual axes:

- established exact preservation;
- neural compression ratio;
- lossy neural throughput;
- generative representation depth.

We found no public result that demonstrates ChronoField's complete
combination: **exact RGB reconstruction, Full-HD compression advantage over
lossless AV1, faster encode, faster decode, and an additional exact
family-storage layer**.

That is the category ChronoField is building.

## Primary sources

- [NeuralLVC paper](https://arxiv.org/html/2604.03353)
- [AV2 v1.0 specification](https://av2.aomedia.org/v1.0.0/index.html)
- [Official AOMedia AV2 release](https://aomedia.org/press%20releases/Alliance-for-Open-Media-Releases-AV2-Codec/)
- [AV2 evaluation paper](https://arxiv.org/abs/2605.15800)
- [Microsoft DCVC official repository](https://github.com/microsoft/DCVC)
- [ByteDance CascadeV official repository](https://github.com/bytedance/CascadeV)
- [MagicYUV official site](https://www.magicyuv.com/)
- [Lagarith official site](https://lags.leetcode.net/codec.html)
- [JPEG 2000 official overview](https://jpeg.org/jpeg2000/index.html)
- [FFV1 standard, RFC 9043](https://www.ietf.org/rfc/rfc9043.html)

The ChronoField measurements are internally reproducible. Complete artifacts,
hashes, and protocol are available for controlled independent reproduction.
