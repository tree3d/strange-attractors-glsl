# Strange Attractor Studio

An interactive 3D viewer for classic chaotic dynamical systems, rendered as physical objects in a photographic studio scene. Everything lives in a single self-contained HTML file.

<p align="center">
  <img src="imgs/halvorsen-1784993604335.png" alt="Halvorsen attractor rendered in gold" width="100%">
</p>

## Gallery

<table>
  <tr>
    <td><img src="imgs/four-wing-1784993108438.png" alt="Four-Wing attractor in wood"></td>
    <td><img src="imgs/rossler-1784993263741.png" alt="Rössler attractor in wood"></td>
  </tr>
  <tr>
    <td align="center"><sub>Four-Wing</sub></td>
    <td align="center"><sub>Rössler</sub></td>
  </tr>
  <tr>
    <td><img src="imgs/dequan-li-1784993363240.png" alt="Dequan Li attractor in dark metal"></td>
    <td><img src="imgs/thomas-1784993746539.png" alt="Thomas attractor in chrome"></td>
  </tr>
  <tr>
    <td align="center"><sub>Dequan Li</sub></td>
    <td align="center"><sub>Thomas</sub></td>
  </tr>
</table>

<p align="center">
  <img src="imgs/halvorsen-1784993565872.png" alt="Halvorsen attractor in dark metal" width="100%">
  <sub>Halvorsen</sub>
</p>

## Features

- **21 attractor systems** — Lorenz, Rössler, Aizawa, Halvorsen, Thomas, Dadras, Chen, Chen-Lee, Four-Wing, Arneodo, Burke-Shaw, Dequan Li, Genesio-Tesi, Hadley, Newton-Leipnik, Nosé-Hoover, Rucklidge, Sprott B, Shimizu-Morioka, Bouali, and Rabinovich-Fabrikant — with the governing equations shown in the header
- **Studio-realistic rendering** — custom GLSL shading with wrap-diffuse lighting from three studio panels, soft shadows, mirror-reflection floor, and tone mapping done in a composite pass
- **Material presets** — switch the attractor between metal, ceramic, glass-like and other finishes
- **Live parameter controls** — sliders for system parameters, plus quality presets (supersampling, shadow map size, mirror resolution)
- **Orbit camera** — drag to rotate around the scene
- **No build step, no dependencies to install** — Three.js (r128) is loaded from a CDN; open the file in a browser and it runs

## Usage

Open `strange-attractors-studio.html` in any modern browser, or serve the directory locally:

```sh
# from this directory
python -m http.server 8000
# then visit http://localhost:8000/strange-attractors-studio.html
```

An internet connection is required on first load to fetch Three.js from cdnjs.

## Controls

| Action | How |
|---|---|
| Rotate camera | Left-drag on the scene |
| Change attractor / material / parameters | Side panel (top-right) |
| Toggle panel on small screens | Button at top-right |

## Files

- `strange-attractors-studio.html` — the entire app: markup, styles, GLSL shaders, and simulation/rendering logic
