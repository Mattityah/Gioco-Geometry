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

A browser-based image effects lab. Upload any image and transform it through three distinct rendering engines: halftone geometry, CRT screen simulation, and ASCII character mapping.

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

Your image becomes a geometric grid. Each cell samples the luminosity of the original and renders a shape — circle, square, arrow, or a custom mix — sized and colored by what it finds there.

|Control       |What it does                                                                     |
|--------------|---------------------------------------------------------------------------------|
|Dithering     |None / Floyd-Steinberg / Bayer — controls how tonal transitions are handled      |
|Grid Type     |Regular or Benday (offset rows — the Roy Lichtenstein effect)                    |
|Shape         |Circle · Square · Arrow · Mix · Custom combination                               |
|Size Texture  |Wave / Noise / Voronoi modulation — makes size vary organically across the canvas|
|Luminance Size|Darker pixels → larger shapes. Lighter pixels → smaller shapes                   |
|Relief        |Emboss effect applied to the grayscale before rendering                          |
|Color         |Mono or multi-palette with 7 customizable swatches                               |

**CRT**

Your image becomes a phosphor screen. The renderer simulates the physical dot structure of cathode ray tubes — the gap between the phosphors, the convergence of the RGB beams, the barrel distortion of the glass.

|Type   |Description                            |
|-------|---------------------------------------|
|Monitor|Staggered circular RGB dots            |
|TV     |Rectangular triads with vertical offset|
|LCD    |Stripe subpixel layout                 |

Bloom, glow, and RGB chromatic aberration are applied as post-processing.

**ASCII**

Your image becomes text. Each cell of a character grid samples the local brightness and maps it to a character from a customizable set — ordered by visual density so the darkest areas get the heaviest characters.

Copy to clipboard or export as `.txt`.

-----

— Features

|Feature         |Description                                                   |
|----------------|--------------------------------------------------------------|
|Image Transform |Scale, position, rotation — independent of canvas size        |
|Canvas Presets  |Instagram · 16:9 · Story · A4 · Banner · Custom W×H           |
|Export          |PNG · JPG (with quality control) · SVG (Halftone) · ASCII .txt|
|Style Presets   |Micro-Geo · Medieval · Pastel · Bold — one tap configurations |
|Preset Save/Load|Export your parameter set as `.json`, import it later         |
|Live Preview    |All controls update the canvas in real time                   |
|Mobile-first    |Designed for phone use. Works on desktop too.                 |
|PWA             |Installable on iOS and Android                                |

-----

— Stack

|Layer    |Tech                                                  |
|---------|------------------------------------------------------|
|Frontend |HTML + CSS + Vanilla JS                               |
|Rendering|Canvas 2D API                                         |
|Dithering|Floyd-Steinberg + Bayer matrix (custom implementation)|
|Textures |Value noise · Fractal Brownian Motion · Voronoi       |
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

More effects in the lab — Stippling, Edge detection, Recolor, Glitch, Displacement, Cellular Automata, Gradients.

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
