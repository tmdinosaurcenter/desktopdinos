# Desktop Dinos — Image Generation Prompt Guide

Use these prompts with image-generation tools (DALL-E, Midjourney, Stable Diffusion, etc.) or as a briefing for an artist AI assistant. Each section builds on a shared base prompt; swap in the species block for each dinosaur.

---

## Base Prompt (include for every species)

```
Pixel art sprite sheet for a desktop companion app. Style: 16-bit era, 
clean 1px dark outline, pillow shading, light source from upper-left, 
transparent background (no background color at all — pure alpha).

Canvas: a single PNG image exactly 1024 pixels wide and 1152 pixels tall.
The image is a grid of 8 columns and 9 rows.
Each cell is exactly 128x128 pixels.
Every cell that is not used by an animation frame must be fully transparent.

The character faces RIGHT in all walking, crawling, and climbing animations.

Row layout (top to bottom):
  Row 1: stand — 1 frame. Neutral idle pose, slight weight on both legs.
  Row 2: walk — 4 frames. Standard walk cycle, feet lift and fall clearly.
  Row 3: sit — 1 frame. Resting or crouching pose.
  Row 4: greet — 4 frames. A friendly greeting gesture appropriate to the species.
  Row 5: jump — 1 frame. Mid-air pose, feet off the ground.
  Row 6: fall — 3 frames. Falling sequence: anticipation, peak, descent.
  Row 7: drag — 1 frame. Being gently dragged sideways, slightly surprised.
  Row 8: crawl — 8 frames. Low crawling cycle along a horizontal surface.
  Row 9: climb — 8 frames. Climbing a vertical surface; rotate the character 
          ~90° clockwise so it faces the wall.

Rows 1, 3, 5, and 7 have only 1 frame each. Fill columns 2–8 in those rows 
with fully transparent 128x128 cells.

Color palette: 6–12 colors per character including shading and highlight tones. 
No dithering required. Outlines are 1px dark (not pure black — use a very dark 
shade of the dominant color). Interior lines are a darker shade of the fill.

The character should be scientifically plausible in silhouette and body plan, 
but friendly and approachable — suitable for a natural history museum audience 
of all ages. Avoid hyper-realism. Avoid cartoonish exaggeration (no googly eyes, 
no oversized heads). Subtle personality in the pose and expression is welcome.

The character body should fill approximately 80–100px of the 128px cell height.
```

---

## Per-Species Additions

Append one of the following blocks to the base prompt.

---

### Daspletosaurus

```
Species: Daspletosaurus torosus. Large tyrannosaurid theropod from the 
Two Medicine Formation of Montana, Late Cretaceous. Bipedal. Large robust 
skull with powerful jaws and small serrated teeth visible. Tiny two-fingered 
forelimbs. Long counterbalancing tail. Suggested palette: warm earthy browns 
and ochres with darker striping along the flanks, pale cream underside.
Greet animation: opens jaws wide and tilts head, then closes — a confident roar.
```

---

### Maiasaura

```
Species: Maiasaura peeblesorum. Large hadrosaur (duck-billed dinosaur) from 
the Two Medicine Formation of Montana, Late Cretaceous. Quadrupedal for stand, 
sit, crawl, and walk; may rear onto hind legs briefly for greet and jump. 
Broad flat bill, small solid crest above the eyes, robust body. 
Suggested palette: warm olive green with darker mottling on the back, 
pale sandy underside, subtle reddish tones around the face.
Greet animation: rears up slightly onto hind legs and bobs its head — 
a nurturing, gentle gesture. Maiasaura means "good mother lizard"; 
the pose should feel warm and welcoming.
```

---

### Hypacrosaurus

```
Species: Hypacrosaurus stebingeri. Large crested hadrosaur from the 
Two Medicine Formation of Montana, Late Cretaceous. Quadrupedal for ground 
states; may rear for greet. Tall hollow rounded crest on top of the skull — 
this is the key distinguishing feature. Long tail, robust limbs.
Suggested palette: deep teal and forest green on the back, fading to pale 
yellow-cream on the underside; the crest is a brighter accent color (burnt 
orange or deep red).
Greet animation: raises and tilts the crested head to show off the crest, 
as if calling — hadrosaur crests were likely resonating chambers.
```

---

### Gryposaurus

```
Species: Gryposaurus notabilis. Large hadrosaur from the Two Medicine 
Formation of Montana, Late Cretaceous. Quadrupedal. Distinguished by a 
prominent arching nasal hump ("hook-nosed" profile) — make this clearly 
visible even in the 128px frame. Robust body, long tail.
Suggested palette: slate grey-blue on the dorsal surface, lighter grey 
underside, with warm tan or rust tones on the nasal hump and face.
Greet animation: turns head to show the distinctive nasal arch in profile, 
then bobs head forward in greeting.
```

---

### Einiosaurus

```
Species: Einiosaurus procurvicornis. Medium ceratopsian from the Two Medicine 
Formation of Montana, Late Cretaceous. Quadrupedal, low to the ground. 
Key features: a single large forward-curving (hook-shaped) nose horn, 
two backward-pointing spikes on the frill, and a wide neck frill. 
No brow horns. Stocky body, short tail.
Suggested palette: dusty tan and sandy brown body, with the frill edged in 
a warm red or orange to suggest display coloration.
Greet animation: lowers head to present the curved horn, then raises it — 
a display gesture.
```

---

### Achelousaurus

```
Species: Achelousaurus horneri. Medium ceratopsian from the Two Medicine 
Formation of Montana, Late Cretaceous. Quadrupedal. Similar to Einiosaurus 
but with a roughened boss (bony bump) instead of a nose horn, and two 
forward-curving spikes on the frill top. Wide frill with a scalloped edge.
Suggested palette: warm sandy brown, darker on the frill with lighter scalloped 
edges; bosses/bumps highlighted in a contrasting grey or bone-white.
Greet animation: swings the wide frill toward the viewer in a lateral display, 
then centers it.
```

---

### Gorgosaurus

```
Species: Gorgosaurus libratus. Medium tyrannosaurid theropod from the 
Two Medicine Formation of Montana, Late Cretaceous. Bipedal. Slender compared 
to Tyrannosaurus — longer legs, proportionally smaller head than Daspletosaurus, 
but still a formidable predator. Two-fingered forelimbs. Long tail.
Suggested palette: cool grey-green on the dorsal surface, pale grey underside, 
with dark banding or striping along the body. Give it a slightly leaner, 
faster look than Daspletosaurus.
Greet animation: bobs head quickly and snaps jaws once — alert and inquisitive 
rather than aggressive.
```

---

### Troodon

```
Species: Troodon formosus. Small troodontid theropod from the Two Medicine 
Formation of Montana, Late Cretaceous. Bipedal. Key features: very large 
eyes relative to head size (enhanced night vision), large brain case, 
grasping hands with a raptorial sickle claw on each foot (held raised 
off the ground). Slender, lightweight build.
Suggested palette: warm amber and tan with darker brown patterning like 
an owl or hawk; the large eyes should stand out — golden iris suggested.
Greet animation: tilts head sharply to one side, blinks the large eye at 
the viewer — curious and clever.
The character is small; allow more negative space around it in the 128px cell.
```

---

### Edmontonia

```
Species: Edmontonia rugosidens. Large nodosaur (ankylosaur without tail club) 
from the Two Medicine Formation of Montana, Late Cretaceous. Quadrupedal, very 
low and wide — heavily armored with rows of osteoderms (bony plates and spikes) 
along the back and sides, and prominent forward-pointing shoulder spikes. 
No tail club. Short thick legs, wide barrel body.
Suggested palette: dark olive-brown armor plates with lighter edges, warm 
tan on the underside and between the scutes.
Due to the wide, low profile, the character may be wider than tall in the cell — 
use more horizontal space and center vertically.
Greet animation: raises one shoulder spike slightly and gives a slow, 
deliberate nod — sturdy and unimpressed.
```

---

### Orodromeus

```
Species: Orodromeus makelai. Small hypsilophodontid (basal ornithopod) from 
the Two Medicine Formation of Montana, Late Cretaceous. Bipedal, fast-moving, 
lightly built. Long slender hind legs, short arms, small head, large eyes. 
Analogous in feel to a small deer or rabbit — alert and nimble.
Suggested palette: warm sandy brown with lighter cream underside; subtle 
dappled patterning on the back for camouflage.
The character is small; allow more negative space around it in the 128px cell.
Greet animation: springs up quickly onto tiptoes and flicks its head up — 
startled-but-friendly energy.
```

---

### Seismosaurus

```
Species: Seismosaurus halli (also known as Diplodocus hallorum). 
Enormous sauropod dinosaur — the TMDC museum specimen. Quadrupedal. 
Exceptionally long neck (roughly half the total body length) and long 
whip-like tail. Tiny head relative to body, pillar-like legs, massive body.

IMPORTANT: Seismosaurus does not fit naturally in a 128px square. 
Use one of these two approaches — pick whichever looks best:

Option A (miniaturized): Draw a stylized miniature version where the 
long neck curves up and back like a question mark so the whole animal 
fits in the cell. The extreme neck length should still be the dominant 
visual feature.

Option B (partial): Show only the front third of the animal (head, neck, 
and front legs), with the body implied to continue off the right edge of 
the frame. The neck should arc gracefully.

Suggested palette: warm grey-brown body with slightly darker dorsal stripe, 
pale underside; skin texture suggested by subtle darker mottling.
Greet animation: slowly swings the long neck from a low position up to 
full height — majestic and unhurried.
Walk animation: due to the body plan, use a slow lumbering 4-frame cycle 
with clear weight shifts on each pillar-leg.
```

---

## Notes for LLM / AI Assistant Use

If using a language model (e.g. ChatGPT, Claude) to help generate or refine these sprites via a tool like DALL-E or Stable Diffusion:

1. **Start with the base prompt**, then append the species block. Do not omit the grid dimensions or row layout — they are load-bearing for how the app parses the file.
2. **Ask for one species at a time.** Generating all 11 in one request produces lower-quality results.
3. **Iterate on the stand frame first.** Get the idle pose and palette right before generating the full sheet. A good stand frame makes it much easier to maintain consistency across rows.
4. **Verify the grid before committing.** Open the PNG in any image editor and check that frames align to the 128px grid. Misaligned frames will play incorrectly in-app.
5. **The transparent background is mandatory.** If the tool produces a white or colored background, remove it in post (use "remove background" or manually set all non-character pixels to alpha=0).
6. **The filename must match exactly** (all lowercase, `.png` extension) — see the spec for the full list.
