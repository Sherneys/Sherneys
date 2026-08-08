<div align="center">

<table>
<tr>
<td width="25%"><img src="https://raw.githubusercontent.com/Sherneys/blue-noise-raytracer/main/image_test/blue_noise_4spp.png" width="100%" alt="Path-traced spheres at 4 samples per pixel, very grainy"></td>
<td width="25%"><img src="https://raw.githubusercontent.com/Sherneys/blue-noise-raytracer/main/image_test/blue_noise_16spp.png" width="100%" alt="The same scene at 16 samples per pixel"></td>
<td width="25%"><img src="https://raw.githubusercontent.com/Sherneys/blue-noise-raytracer/main/image_test/blue_noise_64spp.png" width="100%" alt="The same scene at 64 samples per pixel"></td>
<td width="25%"><img src="https://raw.githubusercontent.com/Sherneys/blue-noise-raytracer/main/image_test/blue_noise_256spp.png" width="100%" alt="The same scene at 256 samples per pixel, nearly converged"></td>
</tr>
<tr>
<td align="center"><sub><b>4</b> spp</sub></td>
<td align="center"><sub><b>16</b> spp</sub></td>
<td align="center"><sub><b>64</b> spp</sub></td>
<td align="center"><sub><b>256</b> spp</sub></td>
</tr>
</table>

### Viritphon Chongpermwattanapol

<sub>Computer Engineering · Chulalongkorn University</sub>

**I write renderers, and I study what our measurements fail to see.**

</div>

<br>

## Sampling

<div align="center">
<table>
<tr>
<td width="50%"><img src="https://raw.githubusercontent.com/Sherneys/blue-noise-raytracer/main/image_test/white_noise_4spp.png" width="100%" alt="Four samples per pixel with white-noise sampling, showing clumped grain"></td>
<td width="50%"><img src="https://raw.githubusercontent.com/Sherneys/blue-noise-raytracer/main/image_test/blue_noise_4spp.png" width="100%" alt="Four samples per pixel with blue-noise sampling, showing finer more even grain"></td>
</tr>
<tr>
<td align="center"><sub>white noise · 4 spp</sub></td>
<td align="center"><sub>blue noise · 4 spp</sub></td>
</tr>
</table>

<sub>Same scene, same four rays per pixel. Only the sub-pixel pattern changed.<br>
The gap is widest exactly where you have nothing to spare.</sub>

**[blue-noise-raytracer](https://github.com/Sherneys/blue-noise-raytracer)** · measured 4 → 256 spp

</div>

<br>

## Light transport

<div align="center">
<img src="https://raw.githubusercontent.com/Sherneys/blue-noise-raytracer/main/image_test2/blue_noise4pps.png" width="82%" alt="A second path-traced scene with a metal sphere, a dielectric sphere and scattered spheres on a green plane">

<sub>Dielectrics, metals, defocus — a second test scene at 4 spp.</sub>

**[pathtracer_milestone](https://github.com/Sherneys/pathtracer_milestone)** · next-event estimation with MIS · Fresnel and total internal reflection · Russian roulette · BVH<br>
**[Stochastic-Differentiable-Triangle-Soup](https://github.com/Sherneys/Stochastic-Differentiable-Triangle-Soup)** · CUDA · sigmoid edge opacity · race-free gradients to vertex positions

</div>

<br>

## Geometry

<div align="center">
<table>
<tr>
<td width="50%"><img src="https://raw.githubusercontent.com/Sherneys/CG-Soup-for-Digital-Dentistry/main/output/igea_density.png" width="100%" alt="Triangle-density heat map over a reconstructed Igea head from six viewpoints"></td>
<td width="50%"><img src="https://raw.githubusercontent.com/Sherneys/CG-Soup-for-Digital-Dentistry/main/output/max-planck_density.png" width="100%" alt="Triangle-density heat map over a reconstructed Max Planck bust from six viewpoints"></td>
</tr>
</table>

<sub>Where a reconstruction actually spends its triangles. Red is dense.</sub>

</div>

A reconstruction can land in the right **place** and still be the wrong **shape** — a
closed loop broken open, an enclosed cavity punctured — and the standard geometric
metrics will score it as correct. I measure that gap with persistent homology, and
work on getting the reconstruction to close it.

<div align="center">

**[cg-soup-curvature-init-study](https://github.com/Sherneys/cg-soup-curvature-init-study)** · a negative result, reported as one: curvature-guided initialization is washed out within the first few hundred steps<br>
**[CG-Soup-for-Digital-Dentistry](https://github.com/Sherneys/CG-Soup-for-Digital-Dentistry)** · multi-view facial reconstruction, COLMAP → differentiable rendering, under 5k triangles

</div>

<br>

## Games

<div align="center">

<img src="https://raw.githubusercontent.com/Sherneys/NarrativeDrivenJam14/main/assets/textures/background/Intro%20Final2.png" width="88%" alt="Hand-painted autumn village street at golden hour from the game Sparrow Spring">

**[Sparrow Spring](https://github.com/Sherneys/NarrativeDrivenJam14)** · Godot · GDScript<br>
<sub>Narrative game built with a small cross-disciplinary team for Narrative Driven Game Jam 14.<br>
<a href="https://canterbury.itch.io/sparrow-spring">Playable on itch.io</a></sub>

<br><br>

<img src="https://raw.githubusercontent.com/Sherneys/ColorInRealLife/main/src/main/resources/city_map.png" width="88%" alt="Pixel-art city map board from the game ColorInRealLife">

**[ColorInRealLife](https://github.com/Sherneys/ColorInRealLife)** · Java · JavaFX<br>
<sub>Turn-based board game adapted from <i>No Time to Relax</i>; an object-oriented design project.</sub>

</div>

<br>

## Hardware

<div align="center">

**[HardwareSynLab-Project](https://github.com/Sherneys/HardwareSynLab-Project)** · Verilog · Basys 3 FPGA<br>
<sub>OV7670 camera over SCCB → dual-port BRAM frame buffer → switchable filters → VGA out, in real time.</sub>

</div>

<br>

---

<div align="center">

<sub>C++ · CUDA · Python · PyTorch · GLSL · Verilog · Java · GDScript</sub>

**[viritphon.1234@gmail.com](mailto:viritphon.1234@gmail.com)**

<sub>Open to research internships in rendering and geometry processing.</sub>

</div>
