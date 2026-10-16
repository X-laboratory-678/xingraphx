# XinGraphX

**Turn reference images and research descriptions into editable scientific figures.**

[中文](README.md) · [Skill instructions](skills/xingraphx/SKILL.md) · [MIT License](LICENSE)

XinGraphX is an AI Agent skill for scientific schematics, workflows, mechanism diagrams and technical roadmaps. It guides content review, layout, native PowerPoint reconstruction and rendered verification. The default deliverables are one single-slide **PPTX** and one high-resolution **PNG** per figure.

## Features

- Reconstruct reference figures while preserving panel structure, colors and visual relationships.
- Organize research descriptions into compact, readable academic layouts.
- Build text, arrows, nodes, axes and schematic curves as native editable PowerPoint objects.
- Use native Office Math for equations, preserving fractions and subscripts.
- Add complex illustrations as separate, movable image assets when needed.
- Inspect the saved PPTX structure and actual rendered output before delivery.
- Export PNGs with a long edge of at least 3600 pixels; meet 300 dpi pixel requirements when physical dimensions are specified.

These are workflow requirements. Actual results depend on the Agent's tools, fonts and renderer; verification records must describe what was actually checked.

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
Use native editable objects for text, equations, nodes and curves.
Deliver a single-slide PPTX and a high-resolution PNG, with structural and rendered checks.
```

```text
Use xingraphx to draw a technical roadmap:
data collection → cleaning → feature extraction → training → evaluation.
Use a compact academic layout with a white background.
Deliver editable PPTX and high-resolution PNG files.
```

## Requirements and scope

The repository contains skill instructions and acceptance criteria. The host Agent needs file access, PPTX creation/editing, rendering and PNG export capabilities. Image generation is optional for complex illustrations. If available, the skill uses the host's presentation and image-generation skills; those tools and skills are not bundled here.

Complex illustrations remain separate image assets. Three-dimensional trajectories default to editable two-dimensional projections. Missing experimental data must never be fabricated; schematic data must be identified in slide notes and delivery records. Inserting figures into Word or merging existing figure collections is outside this skill's scope.

PowerPoint rendering is preferred. When another renderer is used, record it and identify checks that remain unverified. Keep build scripts, assets, content corrections and verification records with the deliverables.

## Contributing and license

Issues and pull requests are welcome. For reproducible reports, provide shareable input, expected behavior, actual output and renderer details.

The skill files were supplied by this repository's maintainer.

Released under the [MIT License](LICENSE). Third-party reference figures, papers and assets retain their respective licenses.
