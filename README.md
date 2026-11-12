## Vijay Kapse
ML engineer · IIT Madras · New York · vijayskofficial@gmail.com · [LinkedIn](https://www.linkedin.com/in/vijay-kapse/)

At Manipal Hospitals I was the first hire on a $33 million government-funded project to detect coronary artery disease with AI. I built a team of 8 and took the project from proof of concept to production. The cardiovascular risk work was published in The Royal College of Radiologists Open, and I established the hospital's AI Center of Excellence. At Subex I then owned the data stack behind a production analytics product handling 180M+ records a day.

I studied computer science and data science at IIT Madras, where my research on hospital pathogens became a publication, and earned my MS at Binghamton on a full-tuition merit scholarship. I also have a first-author paper accepted at HICSS 2027 and a provisional patent in AI for biotechnology.

In open source, I have merged fixes in Microsoft's ONNX Runtime and Apple's MLX, including numeric bugs in ARM64 kernels, and I published quantcost, a tool that measures what quantization really costs on real hardware.

My fixes ship in Microsoft's **ONNX Runtime 1.31** and Apple's **MLX 0.32.4**.

#### ONNX Runtime · Microsoft
**1,024** wrong fp16 outputs in the ARM SVE kernels, fixed by emulating all 16 vector lengths. [#33040](https://github.com/microsoft/onnxruntime/pull/33040)<br>
**32,447** kernel tests CI compiled but never ran. They now gate every PR. [#33052](https://github.com/microsoft/onnxruntime/issues/33052)

#### MLX · Apple
**96/96** integer cases where `logcumsumexp` silently returned a cumulative max. [#4625](https://github.com/ml-explore/mlx/pull/4625)<br>
**1 bit** of state fixed `vmap(irfft)` on odd lengths, a limitation an earlier PR left open. [#4637](https://github.com/ml-explore/mlx/pull/4637)

#### ExecuTorch · Meta
**55x** faster CoreML quantizer. The Meta reviewer built on it to re-enable skipped int8 tests. [#23323](https://github.com/pytorch/executorch/pull/23323)

#### Open
**1.5–2x** faster int8 decode: ONNX Runtime re-dequantized tied lm_head weights on every token. Found with quantcost, fixed upstream, under review. [onnxruntime #33800](https://github.com/microsoft/onnxruntime/pull/33800)

#### Tools
[**forgot**](https://github.com/vijay-kapse/forgot) names a truly missing file in 70% of the commits it flags, vs 42% for a baseline. [![forgot downloads](https://img.shields.io/pepy/dt/forgot?style=flat-square&label=downloads)](https://pepy.tech/projects/forgot)<br>
[**quantcost**](https://github.com/vijay-kapse/EdgeLLM) found int8 runs at 0.47x fp32 on Apple M4, and traced why. [![quantcost downloads](https://img.shields.io/pepy/dt/quantcost?style=flat-square&label=downloads)](https://pepy.tech/projects/quantcost)

#### Papers
[ML risk prediction for cardiovascular disease](https://doi.org/10.1016/j.rcro.2025.100264) · RCR Open 2025 · first author<br>
[Pathogen persistence in hospital microbiomes](https://doi.org/10.1101/2025.10.28.25339026) · medRxiv 2025
