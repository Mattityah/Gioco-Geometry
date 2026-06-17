<div align="center">

# Gioco-Geometry

*Transform any image into geometric art.*

[![Live App](https://img.shields.io/badge/▶%20LIVE%20APP-000000?style=for-the-badge&logoColor=white)](https://mattityah.github.io/Gioco-Geometry)
[![GiocoStudio](https://img.shields.io/badge/GiocoStudio-1a1a1a?style=for-the-badge&logoColor=white)](https://mattityah.github.io/Gioco-Geometry)
[![HTML](https://img.shields.io/badge/HTML%20%2B%20Vanilla%20JS-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://mattityah.github.io/Gioco-Geometry)

</div>

-----

I built this as an experiment.

A way to explore what happens when curiosity, play and simple rules are allowed to become tools.

Gioco-Geometry is not just an image processor.

It is a collection of visual systems that transform images into geometry, patterns and structures — while exposing the logic behind them.

Every effect is both a result and a process.

A demonstration that with enough curiosity, anyone can build their own creative environment.

The kind of tool you open to explore, not to execute.

-----

— What it is

A browser-based image effects lab. Upload any image and transform it through six rendering engines: halftone geometry, literal dithering, a Ben-Day dot screen, a black-mask vectorizer, an organic-shape destroyer, and a printed-circuit generator.

Everything runs locally in your browser. No server. No account. No data collected. No internet required after the first load.

> The output is yours. The process is the point.

-----

— Why it exists

Gioco-Geometry is part of **GiocoStudio** — a space dedicated to making things with intention. *Gioco* is Italian for *play*, and that word sits at the center of everything here.

The studio was born from a belief: that technology is most powerful when it serves human creativity rather than replacing it. That the best tools are the ones that open possibilities rather than close them. That exploration is a valid end in itself.

This app grew out of that philosophy — the desire to build something genuinely useful for people who make things.

-----

— Effects

**Halftone**

Your image becomes a geometric grid. Each cell samples the luminosity of the original and renders a shape — square, circle, arrow, a deterministic mix of shapes, or a custom combination you choose yourself.

|Control       |What it does                                                                  |
|--------------|-------------------------------------------------------------------------------|
|Dithering     |None / Floyd-Steinberg / Bayer — controls how tonal transitions are handled, sampled at grid resolution|
|Grid          |Regular or Benday (offset rows, with adjustable grid angle)                  |
|Shape         |Square · Circle · Arrow · Mix (ordered) · Custom combination of shapes        |
|Shape Size    |Fixed size, or size driven by luminance (separate min/max)                   |
|Size Texture  |Wave / Noise / Voronoi / White-noise modulation — shape size varies organically across the canvas|
|Noise         |Random positional jitter for shapes                                          |
|Color         |Mono / Invert / Multi-color with a customizable palette                      |

**Dithering**

A literal pixel-dithering tool, independent from Halftone's shape grid.

|Control    |What it does                                                              |
|-----------|---------------------------------------------------------------------------|
|Algorithm  |Floyd-Steinberg · Bayer · Atkinson · Jarvis · Stucki · Random · Threshold |
|Pixel      |Square, circle, or diamond-shaped pixels, with adjustable pixel size      |
|Color      |Mono or sampled from the source image                                    |

**Dots**

A controllable Ben-Day / screen-tone field built from circular dots and image luminance.

|Control      |What it does                                              |
|-------------|-----------------------------------------------------------|
|Mode         |Screen · Dense · Hard — controls how dot coverage responds to tone|
|Grid Size    |Spacing of the dot grid                                   |
|Min / Max Dot|Size range the dots scale across                         |
|Noise        |Positional jitter                                         |
|Background micro dots|Optional fine dot texture in empty areas        |

**Solid**

Converts sketches, photos, and thin line drawings into a clean black-fill silhouette — built specifically to feed clean shapes into Halftone, Dithering, or Dots.

|Control          |What it does                                                          |
|-----------------|-------------------------------------------------------------------------|
|Mode             |Fill (flat black mask) · Line (contour only) · Poster (level-based threshold) · Edge (blur → posterize → contour-fill)|
|Color a negro    |Pick a color from the image to convert to black, with adjustable tolerance — or fall back to plain luminance|
|Simplify         |Controls how much detail collapses into larger, cleaner shapes        |
|Smooth / Despeckle / Expand|Morphological cleanup of the resulting mask                 |
|Fill closed holes|Flood-fills enclosed gaps inside the silhouette so it stays solid     |
|Use in Halftone  |Sends the generated mask straight into Halftone/Dithering/Dots as the new source image|

**GiocoFX**

A multi-mode destroyer that turns images into organic shapes.

|Mode   |Description                                                                |
|-------|----------------------------------------------------------------------------|
|Destroy|Blur → posterize levels → stroke contour → smooth → despeckle → expand    |
|Blob   |Same pipeline tuned for soft, rounded organic blob shapes                  |
|Beads  |Hama-bead style grid (diamond, circle, square, hex) with source color, mono, or a quantized custom palette|

Like Solid, GiocoFX can send its result straight into Halftone for a second pass.

**Circuit**

Generates a printed-circuit-board pattern where trace density follows the image's luminance.

|Control      |What it does                                                          |
|-------------|-----------------------------------------------------------------------|
|Grid         |Cell size and trace density                                          |
|Traces       |Trace width and chaos (randomized routing)                           |
|Nodes        |Circle · square · cross · diamond · donut · target · via · mix, at intersections|
|Bus Lines    |Optional horizontal/vertical bus lines with width and gap control     |
|Componentes  |Resistor, capacitor, IC, diode, ground symbols scattered at a set frequency|
|Fragmentation|Overlay characters (electronics symbols, A-Z, 0-9, or mixed) as text, blocks, or both, with displacement and chaos|
|Color        |Mono / Invert / Multi-color with palette                             |

-----

— Features

|Feature         |Description                                                          |
|----------------|------------------------------------------------------------------------|
|Image Transform |Scale, position, rotation — independent of canvas size                |
|Canvas Presets  |Instagram · 16:9 · Story · A4 · Banner · Custom W×H                   |
|Shared Tone Stage|Blur, contrast, brightness, gamma applied before any effect's own pipeline|
|Export          |PNG (with optional transparent background) · JPG (quality control) · SVG (Halftone, Dithering, Dots)|
|Shape Color on Export|Force exported shapes to black or white, independent of how they look on screen|
|Preset Save/Load|Export the active tool's full parameter set as `.json`, import it later|
|Live Preview    |All controls update the canvas in real time, throttled for performance|
|Mobile-first    |Draggable bottom panel, touch-sized controls. Works on desktop too.   |
|PWA             |Installable on iOS and Android                                       |

-----

— Stack

|Layer    |Tech                                                  |
|---------|------------------------------------------------------|
|Frontend |HTML + CSS + Vanilla JS                               |
|Rendering|Canvas 2D API                                         |
|Dithering|Floyd-Steinberg, Bayer, Atkinson, Jarvis, Stucki (custom implementations)|
|Masking  |Morphological dilate/erode, despeckle, flood-fill hole-filling for Solid|
|Hosting  |GitHub Pages                                          |

No frameworks. No dependencies. One file. Every algorithm written from scratch.

-----

— Try it

<div align="center">

[▶ mattityah.github.io/Gioco-Geometry](https://mattityah.github.io/Gioco-Geometry)

*Upload an image → choose an effect → adjust until it feels right → export.*

</div>

-----

— Roadmap

More effects and refinements in the lab.

Session history — reopen your last project exactly where you left it.

-----

<div align="center">

— Author

Built by Mattia under GiocoStudio

*Self-taught · From scratch · With intention*

-----

*Technology at the service of creativity.*
*That’s the only rule.*

</div>
