# Desktop Dinos — Sprite Sheet Specification

## Purpose

This document defines the technical and visual requirements for all dinosaur sprite sheets used in Desktop Dinos. Every artist or AI tool producing sprites for this project must follow this spec exactly so that sprites load, animate, and display correctly in the Phaser 3 engine.

---

## Technical Requirements

### File format

| Property | Value |
|---|---|
| Format | PNG |
| Color mode | RGBA (32-bit, with transparency) |
| Background | Fully transparent (`alpha = 0`) everywhere outside the character |
| Color profile | sRGB |

### Frame size

Each individual animation frame is a **128 × 128 pixel square**. This is the `frameSize` value used in every dino config file. The character should fill most of this space — aim for the body to occupy roughly 80–100 px of the 128 px height, with a small margin for visual breathing room.

### Grid layout

Frames are arranged in a uniform grid:

- **Columns** = number of frames in the longest animation state (the `highestFrameMax`)
- **Rows** = one row per animation state (9 rows total for the standard set)
- Every row is padded with blank (fully transparent) frames to match the column count

The simplest valid sheet is **8 columns × 9 rows = 1024 × 1152 px**. If an animation needs more than 8 frames, widen the sheet to accommodate (e.g. 13 columns = 1664 px wide).

**Total sheet dimensions: `(maxFramesInAnyState × 128)` wide × `1152` px tall**

### Row order (animation states)

Rows must appear in this exact order, top to bottom:

| Row | State | Typical frame count | Description |
|---|---|---|---|
| 1 | `stand` | 1 | Idle standing pose, no motion |
| 2 | `walk` | 4 | Walking cycle, moving right |
| 3 | `sit` | 1 | Resting/sitting pose |
| 4 | `greet` | 4 | Greeting animation (wave, nod, roar, etc.) |
| 5 | `jump` | 1 | Mid-air pose |
| 6 | `fall` | 3 | Falling sequence (anticipation → peak → descent) |
| 7 | `drag` | 1 | Being dragged by the user |
| 8 | `crawl` | 8 | Crawling along a surface |
| 9 | `climb` | 8 | Climbing a vertical surface (e.g. window edge) |

The engine plays animations at **9 frames per second**, looping indefinitely.

### Walk direction convention

All walk/crawl/climb cycles face **right**. The engine mirrors the sprite horizontally when the character moves left — do not draw a left-facing variant.

---

## Visual Style

### Overall aesthetic

**Pixel art, 16-bit era, charming and friendly.** Think of the style used in classic SNES/GBA games or modern pixel-art indie titles — clean outlines, limited but expressive color palettes, readable silhouettes at small sizes. The goal is a character that looks great at its native 128 × 128 size and still reads clearly when scaled down to 64 px on screen.

### Tone

These are desktop companions for a real natural history museum. The style should be:

- **Scientifically plausible in silhouette** — correct body plan for the species (bipedal theropods vs. quadrupedal ceratopsians vs. hadrosaurs, etc.)
- **Friendly and approachable**, not fearsome or hyper-realistic
- Subtle personality is welcome (a Troodon that looks a bit clever, a Maiasaura that looks nurturing), but avoid cartoonish exaggeration like oversized heads or googly eyes

### Color palette

- Each species should have a **distinct, cohesive palette of 6–12 colors** including shading and highlight tones
- Use **pillow shading** (shading follows the form, light source from above-left)
- Outlines: **1 px dark outline** on all exterior edges; interior detail lines may be 1 px in a darker shade of the fill color rather than pure black
- No dithering required, but subtle dithering on large flat areas is acceptable

### Scale and anatomy

Because these are different species with very different body plans, use artistic judgment on how to fill the 128 × 128 frame:

- **Large theropods** (Daspletosaurus, Gorgosaurus): upright bipedal stance, large head, small arms — the head and tail may slightly exceed the frame bounds if needed
- **Hadrosaurs** (Maiasaura, Hypacrosaurus, Gryposaurus): quadrupedal for idle/sit states; bipedal for greet/jump
- **Ceratopsians** (Einiosaurus, Achelousaurus): quadrupedal, low to the ground, prominent frill and horns
- **Ankylosaur** (Edmontonia): very low, wide, armored — horizontal silhouette
- **Small theropods** (Troodon, Orodromeus): small and nimble, can show more negative space
- **Sauropod** (Seismosaurus): the longest dinosaur ever found — consider a side-scrolling walk where the neck stretches beyond the frame, or a stylized miniaturized version that fits the frame with a characteristically long neck as the key visual

### Animation notes

- **stand**: a subtle breathing cycle is welcome (1–2 px chest rise) but a single static frame is also valid
- **walk**: standard 4-frame walk cycle; the feet should clearly lift and fall
- **greet**: species-appropriate gesture — a theropod might open its jaws and tilt its head; a ceratopsian might lower and raise its frill; a hadrosaur might rear up briefly
- **climb**: the character should appear to grip and pull itself upward; rotate the character ~90° clockwise so it faces the surface it is climbing
- **drag**: a single pose showing the character being pulled — slightly limp or surprised expression is fine

---

## Deliverables per Species

For each of the 11 dinosaurs, deliver:

1. `<species>.png` — the completed sprite sheet following this spec
2. (Optional) `<species>-palette.png` — a 1×N swatch strip of the colors used

### File naming (must match exactly)

```
daspletosaurus.png
maiasaura.png
hypacrosaurus.png
gryposaurus.png
einiosaurus.png
achelousaurus.png
gorgosaurus.png
troodon.png
edmontonia.png
orodromeus.png
seismosaurus.png
```

Drop finished files into `public/media/` in the repository root. No code changes are needed — the configs already reference these paths.

---

## Quick-Reference Checklist

Before submitting a sprite sheet:

- [ ] PNG with RGBA transparency (no white or colored background)
- [ ] Frame size exactly 128 × 128 px per cell
- [ ] 9 rows in the correct order (stand, walk, sit, greet, jump, fall, drag, crawl, climb)
- [ ] All rows padded to the same column count with transparent frames
- [ ] Walk/crawl/climb cycle faces right
- [ ] Filename matches the list above exactly (all lowercase)
- [ ] Character fills ~80–100 px of the 128 px frame height
- [ ] Transparent background on all empty space
