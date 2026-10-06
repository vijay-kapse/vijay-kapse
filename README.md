<h1 align="center">Vijay Suryakant Kapse</h1>

<p align="center">
  <b>New York | Techie | IIT Madras</b>
</p>

<p align="center">
  I turn ML research into shipped products.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/vijay-kapse/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="https://github.com/vijay-kapse"><img src="https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"></a>
  <a href="mailto:vijayskofficial@gmail.com"><img src="https://img.shields.io/badge/Email-Reach%20out-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</p>

---

## About

Data scientist and builder who ships end-to-end — from model and data pipeline to a live web app users can click. I work across **machine learning, medical imaging, analytics, and AI agents**, and I like taking research-grade ideas all the way to deployed products on the web.

- Graduated from **IIT Madras**
- Focus: applied ML, LLM/AI agents, computer vision, and data products
- Most projects below are **live demos** — click and try them
- Contributions merged upstream into **Apple's MLX** and **Microsoft's ONNX Runtime**
- Open to roles & collaborations: **vijayskofficial@gmail.com**

---

## Open Source

Upstream contributions to production ML inference libraries — numerical correctness
in SIMD kernels, quantization, and test coverage. Every bug below was reproduced,
fixed and verified against a negative control before submitting.

| Project | Contribution | Status |
|---|---|---|
| **MLX** · Apple | [#4625](https://github.com/ml-explore/mlx/pull/4625) — `logcumsumexp` never promoted integer input, so on CPU it silently computed a *cumulative maximum* (integer `logaddexp` truncates to `max`, verified identical to `cummax` in 96/96 configurations) and on GPU no kernel existed to dispatch to. Made it promote like `logaddexp`. | **Merged** |
| **ONNX Runtime** · Microsoft | [#33040](https://github.com/microsoft/onnxruntime/pull/33040) — Two fp16 bugs in the ARM64 **SVE** MLAS kernels: a Gelu overflow and Erf silently dropping NaNs, both lane-position dependent. Fixed, regenerated the frozen assembly, and added SVE test coverage validated at all 16 vector lengths under QEMU. `+361/−49` | **Merged** |
| **ONNX Runtime** · Microsoft | [#33047](https://github.com/microsoft/onnxruntime/pull/33047) — The SVE assembly generator compiled its input translation units as C++17, breaking any use of `std::numbers`. | **Merged** |
| **ONNX Runtime** · Microsoft | [#33052](https://github.com/microsoft/onnxruntime/issues/33052) — Found that `onnxruntime_mlas_test` was built in CI but never executed. **32,447 MLAS tests** went from never-run to gating every PR. Fixed by the maintainers in #33054. | **Resolved** |

**Also open for review:** [MLX #4637](https://github.com/ml-explore/mlx/pull/4637) (`vmap` of an inverse real FFT to an odd length returns the wrong shape) · [ExecuTorch #23323](https://github.com/pytorch/executorch/pull/23323) (CoreML quantizer pattern-graph caching) · [torchao #4970](https://github.com/pytorch/ao/pull/4970) & [#4971](https://github.com/pytorch/ao/pull/4971) (pt2e observers silently dropping complex input; deprecated pytree registration) · [ONNX Runtime #33050](https://github.com/microsoft/onnxruntime/pull/33050) (fp16 exp non-finite coverage)

---

## Featured Projects

| Project | What it does | Live Demo | Code |
|---|---|---|---|
| **EdgeLLM** — On-device LLM inference | Quantizes Qwen2.5-0.5B to INT8/INT4 (**4× smaller, 2× faster**, perplexity 19.0 → 20.1) and runs it from Python, a C++17 KV-cache harness, Android, and a Qualcomm Snapdragon NPU — every number measured on real hardware, never estimated. | [Live ↗](https://edgellm.vercel.app) | [Repo](https://github.com/vijay-kapse/EdgeLLM) |
| **RadAssist** — Medical Imaging AI | AI radiology assistant that analyzes medical images and generates structured reports (Next.js 16 + Vercel AI SDK + Gemini). | [Live ↗](https://medical-images-ai-agent.vercel.app) | [Repo](https://github.com/vijay-kapse/Medical_Images_AI_agent) |
| **ClickCron** | Record a browser task once, replay it forever — turn any repetitive browser flow into a one-command automation. | [Live ↗](https://clickcron.vercel.app) | [Repo](https://github.com/vijay-kapse/ClickCron) |
| **Cattle Retinal CVD Classifier** | Deep-learning pipeline classifying cardiovascular-disease markers from cattle retinal images. | [Live ↗](https://catal-ml.vercel.app) | [Repo](https://github.com/vijay-kapse/CVD-Classification-Of-Cattle-Retinal-Images) |
| **QOR** | Interactive quality/ops review web app. | [Live ↗](https://qor-woad.vercel.app) | [Repo](https://github.com/vijay-kapse/QOR) |
| **Battery Career Skill Tree** | Gamified, RPG-style skill map for careers in the battery industry. | [Live ↗](https://battery-career-skill-map.vercel.app) | [Repo](https://github.com/vijay-kapse/battery-career-skill-tree) |
| **Career Metro (NENY)** | Metro-map style explorer for navigating career paths. | [Live ↗](https://neny-kappa.vercel.app) | [Repo](https://github.com/vijay-kapse/NENY) |
| **Review Management System** | Full review-management dashboard (RMS). | [Live ↗](https://review-management-system-rms.vercel.app) | [Repo](https://github.com/vijay-kapse/Review-Management-System-RMS) |
| **CPA FAQ Bot** | RAG-based SaaS accounting assistant that answers CPA/finance FAQs. | — | [Repo](https://github.com/vijay-kapse/cpa_faq_bot) |

> More experiments and ML notebooks on my [repositories page ↗](https://github.com/vijay-kapse?tab=repositories).

---

## Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![ONNX](https://img.shields.io/badge/ONNX%20Runtime-005CED?style=flat-square&logo=onnx&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)
![OpenAI](https://img.shields.io/badge/LLMs%20%26%20Agents-412991?style=flat-square&logo=openai&logoColor=white)

**Areas:** Machine Learning · Deep Learning / Computer Vision · LLM & AI Agents · Model Quantization & On-Device Inference · Data Analytics · Full-Stack Web (Next.js)

---

## GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=vijay-kapse&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&hide_rank=true" alt="GitHub Stats" height="165">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=vijay-kapse&layout=compact&theme=tokyonight&hide_border=true" alt="Top Languages" height="165">
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com/?user=vijay-kapse&theme=tokyonight&hide_border=true" alt="GitHub Streak">
</p>

---

<p align="center">
  💬 Let's build something — <a href="https://www.linkedin.com/in/vijay-kapse/">connect on LinkedIn</a> or email <b>vijayskofficial@gmail.com</b>
</p>
