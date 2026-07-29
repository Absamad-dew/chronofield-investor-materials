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

The ChronoField measurements above were collected on a Lenovo consumer laptop
with an **AMD Ryzen 7 H 255 (8 cores / 16 threads), integrated Radeon 780M and
16 GB of system memory**, not on server-class hardware. CFT and AV1 used the
same host. These are measured laptop results; any server or discrete-GPU
uplift remains a separate reproduction and optimization milestone.

The separate CFMS family-storage layer then removes redundancy across related
renditions after the individual streams have already been compressed. In the
current benchmark—two real source excerpts and 20 exact related renditions in
several deterministic production variants—independent CFT11 compact files
required **45.14 MB**. The complete CFMS catalog, including manifests and
index, required **7.38 MB**: an additional **83.65% reduction after CFT** and
**34.85× smaller than raw RGB**. All 20 outputs reconstructed exactly,
aggregate compact decode measured **261 fps**, and all 18 derived renditions
added zero object payload.

That second-layer result applies to related renditions created through known
production transformations. It is aimed at ABR ladders, previews, crops and
version families; it is not a universal ratio for arbitrary independently
re-encoded external files.

## What public competitors optimize

| System | Reconstruction | Public evidence | Commercial implication |
| --- | --- | --- | --- |
| **Lossless AV1** | Exact in the audited configuration | Direct ChronoField baseline | ChronoField wins all 225 recorded size comparisons and has simultaneous Full-HD size/speed wins |
| **FFV1** | Exact, intra-frame | IETF-standardized preservation codec | Mature archival incumbent, not the compression frontier in the reviewed evidence |
| **H.264 / H.265 lossless** | Exact in lossless profiles | Traditional exact video baselines | Strong ecosystem, but no reviewed report reproduces ChronoField's complete Full-HD combination |
| **NeuralLVC (2026)** | Exact YUV420 video; RGB exactness reported for still images | 29.71% of raw YUV420 on nine Xiph CIF sequences; approximately 0.06 fps on NVIDIA GH200 | The most relevant published neural exact-video competitor found, but currently offline-scale |
| **VVC QP=0 in NeuralLVC** | Near-lossless, not exact in that test | 27.24% of raw YUV420 on Xiph CIF | Strong numeric rate, disqualified where byte-exact reconstruction is required |
| **Microsoft DCVC-RT** | Lossy | 125.2 fps encode / 112.8 fps decode at 1080p on NVIDIA A100; 21% bitrate saving against VTM in rate-distortion evaluation | Fast neural delivery, but not an exact-lossless substitute |
| **ByteDance CascadeV** | Generative/lossy | 1024x latent dimensionality reduction; imperfect reconstruction; almost one minute for eight 1024x1024 frames on one NVIDIA A800 | Extreme latent representation by giving up pixel identity |
| **MagicYUV / UT Video / Lagarith / HuffYUV** | Exact capture/intermediate codecs | Public positioning prioritizes recording and editing throughput | Important speed incumbents, but no reviewed report reproduces the complete ChronoField combination |
| **Motion JPEG 2000 / JPEG XL sequences** | Exact per-frame lossless coding | Mature image/archive systems with independent frame codestreams | Strong random access, but no native cross-frame redundancy |
| **ChronoField CFT + CFMS** | Exact RGB plus exact family storage | Direct Full-HD AV1 gates; complete 20-rendition CFMS catalog at 7.38 MB vs 45.14 MB independent CFT | Density, practical speed, and cross-rendition economics in one stack |

NeuralLVC and ChronoField have not yet been run on the same corpus, resolution
or pixel domain, so their compression percentages are not presented as a
direct byte-ratio head-to-head. The hardware context is nevertheless material:
the published NeuralLVC video speed is measured on an NVIDIA GH200, while the
current ChronoField results are local laptop measurements.

## Conclusion

The reviewed competitors are strong on individual axes:

- established exact preservation;
- neural compression ratio;
- lossy neural throughput;
- generative representation depth.

We found no public result that demonstrates ChronoField's complete
combination: **exact RGB reconstruction, Full-HD compression advantage over
lossless AV1, faster encode, faster decode, and an additional exact
family-storage layer with a measured 83.65% reduction across a 20-rendition
production family after individual CFT compression**.

That is the category ChronoField is building.

## Primary sources

- [NeuralLVC paper](https://arxiv.org/html/2604.03353)
- [Microsoft DCVC official repository](https://github.com/microsoft/DCVC)
- [ByteDance CascadeV official repository](https://github.com/bytedance/CascadeV)
- [MagicYUV official site](https://www.magicyuv.com/)
- [Lagarith official site](https://lags.leetcode.net/codec.html)
- [JPEG 2000 official overview](https://jpeg.org/jpeg2000/index.html)
- [FFV1 standard, RFC 9043](https://www.ietf.org/rfc/rfc9043.html)

The ChronoField measurements are internally reproducible. Complete artifacts,
hashes, and protocol are available for controlled independent reproduction.
