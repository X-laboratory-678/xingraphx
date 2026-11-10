# 万象归鑫 · XinGraphX

**科研万象，一绘归鑫。**

Reconstruct scientific figures with template fidelity as the highest goal: keep text and simple structures native and generate every pictorial icon and illustration immediately.

[中文](README.md) · [Skill instructions](skills/xingraphx/SKILL.md) · [MIT License](LICENSE)

XinGraphX is an AI Agent skill for scientific schematics, workflows, mechanism diagrams and technical roadmaps. It guides content review, layout, native PowerPoint reconstruction and rendered verification. The default deliverables are one single-slide **PPTX** and one high-resolution **PNG** per figure.

## Features

- Faithfully reconstruct template layout, background, positions, proportions, spacing, hierarchy, colors and visual relationships; flag issues before changing them.
- Organize research descriptions into compact, readable academic layouts.
- Build text, connecting arrows, node frames, data charts, axes and schematic curves as native editable PowerPoint objects; handle icons inside nodes separately.
- Use native Office Math for equations, preserving fractions and subscripts.
- Generate every pictorial icon and illustration immediately, including simple ones, and insert each as a separate, movable image asset.
- Inspect the saved PPTX structure and actual rendered output before delivery.
- Export PNGs with a long edge of at least 3600 pixels; meet 300 dpi pixel requirements when physical dimensions are specified.

These are workflow requirements. Actual results depend on the Agent's tools, fonts and renderer; verification records must describe what was actually checked.

## Generate pictorial assets immediately

Generate equipment, suns, battery appearances, people, organs and other pictorial icons or illustrations immediately, regardless of apparent simplicity. Do not first assemble them from PowerPoint shapes, SVG or programmatic drawings. Keep text, Office Math equations, data charts, axes, curves, standard scientific symbols, abstract nodes, points, lines, areas and arrows native and editable. A standard battery circuit symbol can be native; a pictorial battery icon must be generated. Purely abstract workflows do not need image generation.

Generation proceeds without per-asset approval. Use the corresponding template region to guide each asset's contour, perspective, proportions, colors and key details. Assets default to transparent backgrounds without text; keep labels, node frames and connections separate. Images can be moved or replaced, but their internal details are not individually editable. Do not rasterize an entire slide, workflow or large panel, or deliver cropped template regions as reconstructed assets. Crops may be used as generation references only.

After the first generation, allow at most three targeted correction rounds per asset, for a maximum of four generations; stop once it meets the target. Record specific differences at each round. If significant differences remain or generation tools are unavailable, keep the best candidate, continue independent work and ask the user to decide on the unresolved differences. Do not fall back to shape-based drawings or mark an inadequate asset as passed. Explicit requests for fully native output take precedence; explain conflicts and confirm the tradeoff.

## Template fidelity

Perfect reconstruction is the highest goal for reference tasks. Preserve the template's layout, background, positions, proportions, spacing, hierarchy, colors and visual relationships. Do not independently beautify, restyle or rearrange it. Flag typos, occlusion or scientific issues for the user to decide before changing them. Tasks based only on text retain the existing content-led layout approach.

Compare the final PPT rendering with the template side by side and, when useful, as an overlay. Check the whole composition, then inspect each asset's contour, perspective, proportions, colors, transparency edges, key details and scientific structure at its final display size. Record remaining differences; generation or export success alone is not proof of perfect reconstruction.

## Edit continuous text as a block

Use one native text box for a continuous paragraph, list or explanatory block within a node, rather than one box per displayed line. Keep size, weight and color changes as local text formatting. Small inline font changes, such as English terms within Chinese text, stay in the same box; separate blocks with different font families use separate boxes.

Do not merge across nodes, panels, columns or independently positioned regions. Keep titles, figure captions, tick labels, legend entries and standalone annotations separate. Use paragraphs, line spacing, indentation and text-box dimensions instead of space padding or grouping multiple boxes. Check wrapping, overflow, font substitution and alignment after merging; preserve native equation structures.

## Speaker notes for presentations

When a task includes a talk, lecture, defense or report deck, automatically write a complete, natural spoken script in every slide's native PowerPoint notes, beginning with a suggested duration. Explain the slide and its charts, connect adjacent slides, and include brief scripts for covers, agendas and transitions. Give key charts and conclusions more time according to their importance and difficulty.

Ask for the speaking duration if it is missing, and wait for it before finalizing the scripts. Treat the stated duration as speaking time unless it explicitly includes Q&A; deduct included Q&A first, then reserve about 10% for pauses and slide changes. For Chinese, estimate around 220 characters per minute and slow down for technical material. Use a suitable estimate for other spoken languages. Timing estimates do not guarantee live delivery duration.

When editing a deck, retain applicable existing narration and adjust it to the revised slides and timing. Preserve sources and schematic-data disclosures as separate paragraphs, excluding them from spoken-length estimates. Read back the saved notes to verify completeness, slide order and the overall timing budget. Standalone scientific figures retain their existing workflow; explicit requests for graphics-only work or no scripts take precedence.

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
Generate every pictorial icon and illustration immediately as a separate asset; do not first try shapes.
Keep labels and connections editable, preserve the template background and layout, and compare the final PPT rendering with the reference.
Deliver a single-slide PPTX and a high-resolution PNG, with structural and rendered checks.
```

```text
Use xingraphx to draw a technical roadmap:
data collection → cleaning → feature extraction → training → evaluation.
Use a compact academic layout with a white background.
Deliver editable PPTX and high-resolution PNG files.
```

For a talk, specify the duration, for example:

```text
Use xingraphx to refine this academic presentation for a 20-minute talk, with Q&A separate.
Write a complete spoken script in every slide's native notes, beginning with a suggested duration.
Allocate time by importance and difficulty, preserve sources and disclosures, and verify the saved notes.
```

## Requirements and scope

The repository contains skill instructions and acceptance criteria. The host Agent needs file access, PPTX creation/editing, rendering and PNG export capabilities. Every pictorial icon and illustration requires image generation; purely geometric workflows and standard scientific symbols do not. If available, the skill uses the host's presentation and image-generation skills; those tools and skills are not bundled here. Preserve template backgrounds in reference tasks; text-only tasks default to white.

Complex illustrations remain separate image assets. Three-dimensional trajectories default to editable two-dimensional projections. Missing experimental data must never be fabricated; schematic data must be identified in slide notes and delivery records. Inserting figures into Word or merging existing figure collections is outside this skill's scope.

PowerPoint rendering is preferred. When another renderer is used, record it and identify checks that remain unverified. Keep build scripts, assets, native/generated responsibilities, reference regions, per-round differences, correction counts, final-size checks and confirmed content corrections with the deliverables. Identify native objects and image assets in the delivery notes.

## Contributing and license

Issues and pull requests are welcome. For reproducible reports, provide shareable input, expected behavior, actual output and renderer details.

The skill files were supplied by this repository's maintainer.

Released under the [MIT License](LICENSE). Third-party reference figures, papers and assets retain their respective licenses.
