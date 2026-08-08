<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=190&section=header&text=Viritphon%20Chongpermwattanapol&fontSize=38&fontColor=ffffff&fontAlignY=34&desc=Computer%20Graphics%20%C2%B7%20Differentiable%20Rendering%20%C2%B7%20Game%20Development&descSize=15&descAlignY=54&animation=fadeIn" alt="Viritphon Chongpermwattanapol — Computer Graphics, Differentiable Rendering, Game Development" width="100%" />

[![Chulalongkorn University](https://img.shields.io/badge/Chulalongkorn_University-Computer_Engineering-E1489C?style=for-the-badge&logoColor=white)](https://www.chula.ac.th/)
![Intania108](https://img.shields.io/badge/Intania108-CP51-FF6F00?style=for-the-badge)
![Open to Research Internships](https://img.shields.io/badge/Open_to-Research_Internships-2EA043?style=for-the-badge)

[![Email](https://img.shields.io/badge/Email-viritphon.1234@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:viritphon.1234@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-Sherneys-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Sherneys)
[![itch.io](https://img.shields.io/badge/itch.io-Sparrow_Spring-FA5C5C?style=flat-square&logo=itchdotio&logoColor=white)](https://canterbury.itch.io/sparrow-spring)
![Profile views](https://komarev.com/ghpvc/?username=Sherneys&style=flat-square&color=6E7BF2&label=Profile+Views)

</div>

<div align="center">

`differentiable rendering` &nbsp;·&nbsp; `ray & path tracing` &nbsp;·&nbsp; `real-time rendering` &nbsp;·&nbsp; `game development`

<br>

**[🔬 Research](#-research)** &nbsp;•&nbsp; **[🖼️ Graphics](#️-computer-graphics-projects)** &nbsp;•&nbsp; **[🎮 Games](#-game-development-projects)** &nbsp;•&nbsp; **[🛠️ Skills](#️-technical-skills)** &nbsp;•&nbsp; **[📫 Contact](#-get-in-touch)**

</div>

---

## 🧠 About Me

I'm an engineering student fascinated by how code brings virtual worlds to life. My focus sits at the intersection of **computer graphics** and **game development** — from Monte Carlo light transport and GPU differentiable rendering to gameplay systems and interactive storytelling.

I love where mathematics, physics, and art meet in real-time graphics: writing renderers from scratch, tuning sampling strategies, and shipping games that are both technically interesting and fun to play. Lately my research asks two questions with surprising answers: *do the metrics we trust in 3D reconstruction actually see topology?* (**No.**) *And can a resampling prior fix what they miss?* (**Yes**, for enclosed voids — if you *spread* it rather than concentrate it.)

<table>
<tr>
<td width="33%" align="center">

**🔬 Research**

Topology-aware<br>triangle-soup reconstruction<br><sub>paper draft in progress</sub>

</td>
<td width="33%" align="center">

**🖼️ Graphics**

CUDA · path tracing<br>real-time rendering<br><sub>renderers built from scratch</sub>

</td>
<td width="33%" align="center">

**🎮 Games**

Godot · Unity · JavaFX<br>gameplay & narrative systems<br><sub>jam-shipped and course-built</sub>

</td>
</tr>
</table>

---

## 🔬 Research

### [CG-Soup-Topology](https://github.com/Sherneys/CG-Soup-Topology)

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![GUDHI](https://img.shields.io/badge/GUDHI-persistent_homology-8E44AD?style=flat-square)
![Status](https://img.shields.io/badge/Phases_1–2b-complete-2EA043?style=flat-square)

Undergraduate research on **topology-aware resampling** for differentiable triangle-soup reconstruction — now a full thread (Phases 1–2b) with a paper draft: *"Concentrate or Spread? Shaping Topological Resampling Priors for Differentiable Triangle-Soup Reconstruction."*

<details open>
<summary><b>Four results</b></summary>

<br>

**1 · Standard geometric metrics are topologically blind.** At equal Chamfer distance, persistence-diagram distance separates correct from topologically-wrong reconstructions by **~30–40×** — and Hausdorff95 even *prefers* the wrong candidate in 2 of 3 cases.

**2 · Init-only bias doesn't survive.** A topological bias applied at initialization is erased by the first resampling step — guidance must be **in-loop**.

**3 · In-loop persistence guidance works, but selectively.** A persistence-guided resampling prior gives a genuine topology-specific win for **enclosed voids**, but backfires on loops at tight budgets.

**4 · Spread beats concentrate.** Spreading the prior cuts bottleneck-to-target **33–53% below baseline** for voids at Chamfer parity — though a width-matched non-topological control recovers most of the gain, leaving only a small topological residual. *Reporting that caveat honestly is the paper's thesis.*

</details>

<br>

### [cg-soup-curvature-init-study](https://github.com/Sherneys/cg-soup-curvature-init-study)

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Negative result](https://img.shields.io/badge/negative_result-reproducible-6E7BF2?style=flat-square)

A reproducible **negative-result study**: against analytic ground truth, curvature-guided initialization does **not** improve DiffSoup reconstruction over random initialization — the apparent benefit against screened-Poisson references was largely an artifact of fitting reconstruction noise. Reporting what *doesn't* work is part of doing research honestly.

<br>

### [CG-Soup-for-Digital-Dentistry](https://github.com/Sherneys/CG-Soup-for-Digital-Dentistry)

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![COLMAP](https://img.shields.io/badge/COLMAP-SfM-4A90D9?style=flat-square)
![Open3D](https://img.shields.io/badge/Open3D-1F6FEB?style=flat-square)
![Internship](https://img.shields.io/badge/14--week_internship-Jun–Sep_2026-FF6F00?style=flat-square)

14-week intern project applying the triangle-soup pipeline to clinical 3D reconstruction: multi-view facial capture → COLMAP SfM → curvature-guided DiffSoup targeting **<5,000-triangle** facial models — integrated with fiducial-marker jaw tracking (iPhone TrueDepth, per-frame 6-DOF via SVD).

---

## 🖼️ Computer Graphics Projects

### [Stochastic-Differentiable-Triangle-Soup](https://github.com/Sherneys/Stochastic-Differentiable-Triangle-Soup)

![CUDA](https://img.shields.io/badge/CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)

A **differentiable** triangle renderer using stochastic opacity masking — soften edges with `α = sigmoid(d/σ)`, make a Bernoulli decision, and push gradients back to update vertex positions on the GPU (race-free via `atomicAdd`). Built incrementally against a CPU reference, every step verified. Challenge from **Umetani Lab**, based on *DiffSoup* (Tojo, Bickel, Umetani — CVPR 2026). This renderer underpins my research above.

<br>

### [blue-noise-raytracer](https://github.com/Sherneys/blue-noise-raytracer)

![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Sampling](https://img.shields.io/badge/blue_noise-vs_white_noise-6E7BF2?style=flat-square)

A ray tracer based on *Ray Tracing in One Weekend*, extended to compare **blue-noise vs white-noise** sub-pixel sampling for anti-aliasing. Renders the same scene with both strategies across **4–256 SPP** and measures how fast each converges to a ground-truth reference.

<br>

### [pathtracer_milestone](https://github.com/Sherneys/pathtracer_milestone)

![C++17](https://img.shields.io/badge/C++17-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![MIS](https://img.shields.io/badge/NEE-MIS_power_heuristic-8E44AD?style=flat-square)
![Reproducible](https://img.shields.io/badge/bit--for--bit-reproducible-2EA043?style=flat-square)

A CPU **path tracer**: next-event estimation with an **MIS power heuristic**, dielectric BSDF with Fresnel–Schlick and total internal reflection, Russian-roulette termination, and BVH acceleration — producing bit-for-bit reproducible radiance across prescribed test scenes. Built for a graphics course at Chulalongkorn University.

---

## 🎮 Game Development Projects

### [Sparrow Spring](https://github.com/Sherneys/NarrativeDrivenJam14)

![Godot](https://img.shields.io/badge/Godot-478CBF?style=flat-square&logo=godotengine&logoColor=white)
![GDScript](https://img.shields.io/badge/GDScript-478CBF?style=flat-square)
[![Play on itch.io](https://img.shields.io/badge/▶_Play-itch.io-FA5C5C?style=flat-square&logo=itchdotio&logoColor=white)](https://canterbury.itch.io/sparrow-spring)

A cozy narrative-driven **visual novel** by team Canterbury, developed collaboratively across Art, Narrative, and Programming. Submitted to **Narrative Driven Game Jam 14**.

<br>

### [ColorInRealLife](https://github.com/Sherneys/ColorInRealLife)

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![JavaFX](https://img.shields.io/badge/JavaFX-5382A1?style=flat-square)
![OOP](https://img.shields.io/badge/design-object--oriented-6E7BF2?style=flat-square)

A turn-based game adapted from *No Time to Relax*, built to apply Object-Oriented Programming principles with a JavaFX UI.

---

## 🛠️ Technical Skills

<div align="center">

**Graphics & GPU**

![CUDA](https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white)
![OpenGL](https://img.shields.io/badge/OpenGL-5586A4?style=for-the-badge&logo=opengl&logoColor=white)
![GLSL](https://img.shields.io/badge/GLSL_%2F_HLSL-1F6FEB?style=for-the-badge)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)

**Engines**

![Unity](https://img.shields.io/badge/Unity_(URP)-000000?style=for-the-badge&logo=unity&logoColor=white)
![Godot](https://img.shields.io/badge/Godot-478CBF?style=for-the-badge&logo=godotengine&logoColor=white)

**Languages**

![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=black)
![C#](https://img.shields.io/badge/C%23-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![GDScript](https://img.shields.io/badge/GDScript-478CBF?style=for-the-badge&logo=godotengine&logoColor=white)
![Verilog](https://img.shields.io/badge/Verilog-B31E24?style=for-the-badge)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![MATLAB](https://img.shields.io/badge/MATLAB-0076A8?style=for-the-badge&logo=mathworks&logoColor=white)

**Tools & Platforms**

![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![COLMAP](https://img.shields.io/badge/COLMAP-4A90D9?style=for-the-badge)
![Open3D](https://img.shields.io/badge/Open3D-1F6FEB?style=for-the-badge)
![GUDHI](https://img.shields.io/badge/GUDHI-8E44AD?style=for-the-badge)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)

</div>

**Math for graphics** — linear algebra · transformations · sampling theory · Monte Carlo methods · persistent homology · procedural generation

**Coursework** — Data Structures & Algorithms · Programming Methodology · OOP · Operating Systems & System Programming · Database Systems · Statistics & Applications

---

## 🎯 Currently Working On

| | |
|---|---|
| 📝 | Polishing the **paper draft** from my topology research (*Concentrate or Spread?*) — Phases 1–2b complete, B0–B5 condition sweeps done |
| 🦷 | 3D facial reconstruction for **digital dentistry** — 14-week internship, through Sep 2026 |
| ⚡ | Going deeper into **physically based rendering** and **GPU programming** |

---

## 🌱 Other Projects

Beyond graphics and games, I also build systems and full-stack projects.

**[HardwareSynLab-Project](https://github.com/Sherneys/HardwareSynLab-Project)** &nbsp;![Verilog](https://img.shields.io/badge/Verilog-B31E24?style=flat-square) ![Basys 3](https://img.shields.io/badge/Basys_3-FPGA-CC0000?style=flat-square)
A real-time OV7670-camera → VGA pipeline with switchable image filters: SCCB configuration, dual-port BRAM frame buffer, VGA output.

**[HKT-Lottery](https://github.com/Sherneys/HKT-Lottery)** &nbsp;![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white) ![AWS](https://img.shields.io/badge/AWS_EC2-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
A full-stack lottery application deployed on AWS EC2.

---

## 📫 Get in Touch

<div align="center">

[![Email](https://img.shields.io/badge/viritphon.1234@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:viritphon.1234@gmail.com)
[![Phone](https://img.shields.io/badge/098--998--2288-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](tel:+66989982288)
[![GitHub](https://img.shields.io/badge/Sherneys-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Sherneys)

<br>

⭐ **Feel free to explore my repositories and connect — especially if you're into graphics or games!**

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=110&section=footer" alt="" width="100%" />

</div>
