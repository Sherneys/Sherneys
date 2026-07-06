# Hi 👋 I'm Viritphon Chongpermwattanapol

🎓 Computer Engineering Student at Chulalongkorn University (Intania108 | CP51)
🔬 Undergraduate researcher in **differentiable rendering** — topology-aware triangle-soup reconstruction
🎮 Building **Computer Graphics** & **Games** — renderers, shaders, and gameplay systems
💻 Differentiable rendering · ray/path tracing · real-time rendering · game development
🚀 Actively seeking research internship opportunities

---

## 🧠 About Me

I'm an engineering student fascinated by how code brings virtual worlds to life. My focus sits at the intersection of **computer graphics** and **game development** — from Monte Carlo light transport and GPU differentiable rendering to gameplay systems and interactive storytelling.

I love where mathematics, physics, and art meet in real-time graphics: writing renderers from scratch, tuning sampling strategies, and shipping games that are both technically interesting and fun to play. Lately my research asks a simple question with a surprising answer: *do the metrics we trust in 3D reconstruction actually see topology?* (Spoiler: no.)

---

## 🔬 Research

🔹 **[CG-Soup-Topology](https://github.com/Sherneys/CG-Soup-Topology)** · *Python*
Ongoing undergraduate research on **topology-aware adaptive resampling** for differentiable triangle-soup reconstruction. Phase 1 builds a persistent-homology measurement pipeline (GUDHI alpha complexes, H0–H2 persistence diagrams, bottleneck/Wasserstein stability metrics) and shows that **standard geometric metrics are topologically blind**: on controlled cases tuned to *equal Chamfer distance*, persistence-diagram distance separates correct from topologically-wrong reconstructions by **~30–40×** — and Hausdorff95 even prefers the wrong candidate in 2 of 3 cases.

🔹 **[cg-soup-curvature-init-study](https://github.com/Sherneys/cg-soup-curvature-init-study)** · *Python*
A reproducible **negative-result study**: against analytic ground truth, curvature-guided initialization does **not** improve DiffSoup reconstruction over random initialization — the apparent benefit against screened-Poisson references was largely an artifact of fitting reconstruction noise. Reporting what *doesn't* work is part of doing research honestly.

🔹 **[CG-Soup-for-Digital-Dentistry](https://github.com/Sherneys/CG-Soup-for-Digital-Dentistry)** · *Python*
14-week intern project (Jun–Sep 2026) applying the triangle-soup pipeline to clinical 3D reconstruction: multi-view facial capture → COLMAP SfM → curvature-guided DiffSoup targeting <5,000-triangle facial models — integrated with fiducial-marker jaw tracking (iPhone TrueDepth, per-frame 6-DOF via SVD).

---

## 🖼️ Computer Graphics Projects

🔹 **[Stochastic-Differentiable-Triangle-Soup](https://github.com/Sherneys/Stochastic-Differentiable-Triangle-Soup)** · *CUDA*
A **differentiable** triangle renderer using stochastic opacity masking — soften edges with `α = sigmoid(d/σ)`, make a Bernoulli decision, and push gradients back to update vertex positions on the GPU (race-free via `atomicAdd`). Built incrementally against a CPU reference, every step verified. Challenge from **Umetani Lab**, based on *DiffSoup* (Tojo, Bickel, Umetani — CVPR 2026). This renderer underpins my research above.

🔹 **[blue-noise-raytracer](https://github.com/Sherneys/blue-noise-raytracer)** · *C++*
A ray tracer based on *Ray Tracing in One Weekend*, extended to compare **blue-noise vs white-noise** sub-pixel sampling for anti-aliasing. Renders the same scene with both strategies across 4–256 SPP and measures how fast each converges to a ground-truth reference.

🔹 **[pathtracer_milestone](https://github.com/Sherneys/pathtracer_milestone)** · *C++17*
A CPU **path tracer**: next-event estimation with an **MIS power heuristic**, dielectric BSDF with Fresnel–Schlick and total internal reflection, Russian-roulette termination, and BVH acceleration — producing bit-for-bit reproducible radiance across prescribed test scenes. Built for a graphics course at Chulalongkorn University.

---

## 🎮 Game Development Projects

🔹 **[Sparrow Spring](https://github.com/Sherneys/NarrativeDrivenJam14)** · *Godot · GDScript*
A cozy narrative-driven **visual novel** by team Canterbury, developed collaboratively across Art, Narrative, and Programming. Submitted to **Narrative Driven Game Jam 14** — [play on itch.io](https://canterbury.itch.io/sparrow-spring).

🔹 **[ColorInRealLife](https://github.com/Sherneys/ColorInRealLife)** · *Java · JavaFX*
A turn-based game adapted from *No Time to Relax*, built to apply Object-Oriented Programming principles with a JavaFX UI.

---

## 🛠️ Technical Skills

- **Graphics & Games:** Differentiable Rendering, Ray/Path Tracing, Real-Time Rendering, Shaders (HLSL/GLSL), OpenGL, CUDA, Monte Carlo Methods, Game Balance & Design
- **Engines:** Unity (URP), Godot Engine
- **Languages:** C++, C#, CUDA, C, GDScript, Python, Java, Verilog, JavaScript, HTML/CSS, SQL, MATLAB
- **Math for Graphics:** Linear algebra, transformations, sampling theory, persistent homology, procedural generation
- **Tools & Platforms:** PyTorch, GUDHI, COLMAP, Open3D, Visual Studio, IntelliJ, PyCharm, Git, AWS, Firebase, MongoDB, PostgreSQL, Jupyter
- **Coursework:** Data Structures & Algorithms, Programming Methodology, OOP, Operating Systems & System Programming, Database Systems, Statistics & Applications

---

## 🎯 Currently Working On

- **Phase 2** of my topology research — building the topology-aware resampler on top of the Phase-1 measurement pipeline
- 3D facial reconstruction for **digital dentistry** (14-week internship, through Sep 2026)
- Going deeper into physically based rendering and GPU programming

---

## 🌱 Other Projects

Beyond graphics and games, I also build systems and full-stack projects — e.g. **[HardwareSynLab-Project](https://github.com/Sherneys/HardwareSynLab-Project)**, a real-time OV7670-camera→VGA pipeline with switchable image filters on a Basys 3 FPGA (Verilog), and **[HKT-Lottery](https://github.com/Sherneys/HKT-Lottery)** (Node.js + MongoDB on AWS EC2).

---

## 📫 Contact Me

- 📧 Email: viritphon.1234@gmail.com
- 📞 Tel: 098-998-2288

---

⭐ Feel free to explore my repositories and connect — especially if you're into graphics or games!
