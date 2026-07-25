# Strange Attractor Studio

An interactive 3D viewer for classic chaotic dynamical systems, rendered as physical objects in a photographic studio scene. Everything lives in a single self-contained HTML file.

## Features

- **8 attractor systems** — Lorenz, Rössler, Aizawa, Halvorsen, Thomas, Dadras, Chen, and Chen-Lee — with the governing equations shown in the header
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
