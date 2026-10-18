# 万象归鑫 · XinGraphX

**科研万象，一绘归鑫。**

Turn reference images and research descriptions into scientific figures with native editable structures and generated illustration assets where needed.

[中文](README.md) · [Skill instructions](skills/xingraphx/SKILL.md) · [MIT License](LICENSE)

XinGraphX is an AI Agent skill for scientific schematics, workflows, mechanism diagrams and technical roadmaps. It guides content review, layout, native PowerPoint reconstruction and rendered verification. The default deliverables are one single-slide **PPTX** and one high-resolution **PNG** per figure.

## Features

- Reconstruct reference figures while preserving panel structure, colors and visual relationships.
- Organize research descriptions into compact, readable academic layouts.
- Build text, connecting arrows, node frames, data charts, axes and schematic curves as native editable PowerPoint objects; handle icons inside nodes separately.
- Use native Office Math for equations, preserving fractions and subscripts.
- Generate illustrations and appearance-focused icons when native shapes cannot reproduce them well, and insert them as separate, movable image assets.
- Inspect the saved PPTX structure and actual rendered output before delivery.
- Export PNGs with a long edge of at least 3600 pixels; meet 300 dpi pixel requirements when physical dimensions are specified.

These are workflow requirements. Actual results depend on the Agent's tools, fonts and renderer; verification records must describe what was actually checked.

## Choosing the right drawing method

Generate instruments, organs, cells, material illustrations and icons directly when their appearance relies on texture, three-dimensional lighting, irregular contours or complex details. Other appearance assets may receive one native draft and one correction round. If contours, perspective, proportions, colors or key details still visibly differ at the final display size, switch to image generation instead of repeatedly assembling shapes.

Generation within this scope proceeds without per-asset approval. Assets default to transparent backgrounds without text. Keep text, equations, data charts, node frames and process connections native. Images can be moved or replaced, but their internal details are not individually editable. Do not rasterize an entire slide or workflow, or use cropped reference images as reconstructed assets. Explicit requests for fully native output take precedence; report capability limits when necessary.

Allow at most one targeted generation correction per asset. If quality remains inadequate or generation tools are unavailable, continue independent work and report affected assets together for the user to choose an alternative. Do not silently substitute inaccurate simplified icons. Check scientific structure and appearance in the final PPTX at display size; pixel-identical reproduction is not promised.

## Installation

```bash
git clone https://github.com/X-laboratory-678/xingraphx.git
```

Copy the entire `skills/xingraphx/` folder into your Agent's skill directory. Preserve `agents/` and `references/`. For custom profiles, use the profile's actual skill directory. Compare existing versions before replacing local modifications.

Alternatively, ask your Agent to read `skills/xingraphx/SKILL.md` from the local clone and follow its linked references as needed.

## Quick start

```text
Use xingraphx to reconstruct this reference figure.
Preserve the panel layout, colors and arrow relationships.
Use native editable objects for text, equations, node frames and curves.
Generate difficult illustrations and icons as separate assets; keep labels and connections editable.
Deliver a single-slide PPTX and a high-resolution PNG, with structural and rendered checks.
```

```text
Use xingraphx to draw a technical roadmap:
data collection → cleaning → feature extraction → training → evaluation.
Use a compact academic layout with a white background.
Deliver editable PPTX and high-resolution PNG files.
```

## Requirements and scope

The repository contains skill instructions and acceptance criteria. The host Agent needs file access, PPTX creation/editing, rendering and PNG export capabilities. Illustrations and icons that cannot be reproduced well with native shapes need image generation; simple workflows do not. If available, the skill uses the host's presentation and image-generation skills; those tools and skills are not bundled here.

Complex illustrations remain separate image assets. Three-dimensional trajectories default to editable two-dimensional projections. Missing experimental data must never be fabricated; schematic data must be identified in slide notes and delivery records. Inserting figures into Word or merging existing figure collections is outside this skill's scope.

PowerPoint rendering is preferred. When another renderer is used, record it and identify checks that remain unverified. Keep build scripts, assets, reasons for generation or switching, correction counts, final-size checks and content corrections with the deliverables. Identify native objects and image assets in the delivery notes.

## Contributing and license

Issues and pull requests are welcome. For reproducible reports, provide shareable input, expected behavior, actual output and renderer details.

The skill files were supplied by this repository's maintainer.

Released under the [MIT License](LICENSE). Third-party reference figures, papers and assets retain their respective licenses.
