<div align="center">

<table>
<tr>
<td width="33.33%"><img src="https://raw.githubusercontent.com/Sherneys/blue-noise-raytracer/main/image_test/white_noise_4spp.png" width="100%" alt="Path-traced spheres at 4 samples per pixel with white-noise sampling — heavy grain"></td>
<td width="33.33%"><img src="https://raw.githubusercontent.com/Sherneys/blue-noise-raytracer/main/image_test/blue_noise_4spp.png" width="100%" alt="The same scene at 4 samples per pixel with blue-noise sampling — finer, less clumped grain"></td>
<td width="33.33%"><img src="https://raw.githubusercontent.com/Sherneys/blue-noise-raytracer/main/image_test/ground_truth.png" width="100%" alt="The same scene converged — the reference image"></td>
</tr>
<tr>
<td align="center"><sub>white noise · 4 spp</sub></td>
<td align="center"><sub>blue noise · 4 spp</sub></td>
<td align="center"><sub>converged reference</sub></td>
</tr>
</table>

<sub>Same scene, same four samples per pixel, different sub-pixel sampling.<br>
Rendered with <a href="https://github.com/Sherneys/blue-noise-raytracer">a ray tracer I wrote</a>.</sub>

</div>

<br>

# Viritphon Chongpermwattanapol

**Computer Engineering · Chulalongkorn University**

I write renderers, and I study what our measurements fail to see.

Most of my work sits between light transport and geometry — Monte Carlo path
tracing, GPU differentiable rendering, and lately the question of whether the
metrics we trust in 3D reconstruction can see the *shape* of a surface at all,
as opposed to just its position. They largely cannot, and that turned into a
research thread.

<br>

## Renderers

**[pathtracer_milestone](https://github.com/Sherneys/pathtracer_milestone)** — C++17 CPU path tracer.
Next-event estimation with the MIS power heuristic, dielectric Fresnel and
total internal reflection, Russian roulette, BVH. Bit-for-bit reproducible
radiance on graded test scenes.

**[blue-noise-raytracer](https://github.com/Sherneys/blue-noise-raytracer)** — the three images above.
Blue-noise sub-pixel sampling measured against white noise from 4 to 256
samples per pixel. The interesting part is where the gap is widest: at the low
sample counts, exactly where you have nothing to spare.

**[Stochastic-Differentiable-Triangle-Soup](https://github.com/Sherneys/Stochastic-Differentiable-Triangle-Soup)** — CUDA
stochastic differentiable rendering. Sigmoid edge opacity, Bernoulli sampling,
race-free gradients back to vertex positions, with a CPU reference and
kernels verified step by step.

<br>

## Research

<div align="center">
<img src="https://raw.githubusercontent.com/Sherneys/CG-Soup-for-Digital-Dentistry/main/output/igea_density.png" width="88%" alt="Triangle-density heat map over a reconstructed head, six viewpoints, red where triangles are dense">
<br>
<sub>Where a reconstruction actually spends its triangles. Red is dense.</sub>
</div>

<br>

A reconstruction can land in the right *place* and still be the wrong *shape* —
a closed loop broken open, an enclosed cavity punctured — and the standard
geometric metrics will score it as correct. I work on measuring that gap with
persistent homology, and on getting the reconstruction to close it.

**[cg-soup-curvature-init-study](https://github.com/Sherneys/cg-soup-curvature-init-study)** — a negative
result, reported as one. Curvature-guided initialization does *not* beat random
initialization for triangle-soup reconstruction: whatever bias you set up at
the start is washed out within the first few hundred steps. Figures and code
included so the null is checkable.

**[CG-Soup-for-Digital-Dentistry](https://github.com/Sherneys/CG-Soup-for-Digital-Dentistry)** — multi-view
facial reconstruction from COLMAP structure-from-motion through curvature-guided
differentiable rendering, under 5k triangles, plus fiducial-marker jaw tracking.
A 14-week internship project.

<br>

## Games and hardware

**[Sparrow Spring](https://github.com/Sherneys/NarrativeDrivenJam14)** — a narrative game in Godot and
GDScript, built with a small cross-disciplinary team for Narrative Driven Game
Jam 14. [Playable on itch.io](https://canterbury.itch.io/sparrow-spring).

**[ColorInRealLife](https://github.com/Sherneys/ColorInRealLife)** — turn-based board game in Java and
JavaFX, adapted from *No Time to Relax*; an object-oriented design project.

**[HardwareSynLab-Project](https://github.com/Sherneys/HardwareSynLab-Project)** — real-time video on a
Basys 3 FPGA in Verilog: OV7670 capture over SCCB, dual-port BRAM frame buffer,
switchable filters, VGA out.

<br>

## Tools

C++ · CUDA · Python · PyTorch · GLSL · Verilog · Java · GDScript

Monte Carlo methods, sampling theory, linear algebra for graphics, persistent
homology, BVH construction, COLMAP, Blender.

<br>

---

<div align="center">

**[viritphon.1234@gmail.com](mailto:viritphon.1234@gmail.com)**

<sub>Open to research internships in rendering and geometry processing.</sub>

</div>
