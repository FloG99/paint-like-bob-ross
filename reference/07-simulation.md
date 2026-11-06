# Numbers for simulation and robots

For people building virtual painters, procedural or physics paint simulators and robot arms.
Every number carries its source:

| tag | source |
|---|---|
| **[S]** | stated in the narration, cited `SxxExx mm:ss` |
| **[M]** | measured from video frames, either in a study (`studies/`) or for this page (frame time given) |
| **[T]** | public paint-color table per episode (the first source listed in `METHOD.md`) |
| **[D]** | computed from `dataset/steps/` (379 regular episodes, guests excluded); derived from the narration, so counts are lower bounds and times are ±20 s |
| **[E]** | estimate or modeling suggestion; not measured, tune it |

Video is 480×360, so frame measurements are coarse: ±0.4–0.5 in unless stated otherwise.

## 1. Canvas and units
- **Size**: 18×24 in, named in 84 transcripts [S S08E02 00:22, S10E04 00:23, S12E09 00:41]. Used
  landscape by default and portrait (canvas stood on end) when the scene is tall [S S04E08 00:05,
  S11E05 00:09]. 6 of the 16 studies are portrait, 2 of them with an oval mask [M].
- **Coordinates** as on the cards: fractions of the canvas, x to the right, y down, (0,0) top left,
  ±0.05 [M]. Angles below are degrees from horizontal in these coordinates: 0 = toward the right,
  +90 = straight down, −90 = straight up; +30 is a line falling to the right.

| format | W × H | 1 in as fraction of W | 1 in as fraction of H | inches from (x, y) |
|---|---|---|---|---|
| landscape | 24 × 18 in | 1/24 = 0.042 | 1/18 = 0.056 | (24x, 18y) |
| portrait | 18 × 24 in | 1/18 = 0.056 | 1/24 = 0.042 | (18x, 24y) |

Widths below are given as a fraction of the **landscape** width; multiply by 4/3 for portrait.
Suggested raster for a simulator: 50–100 px per inch (1200–2400 px wide), so a liner line is
3–10 px [E].

## 2. Paints
Hex values are the display colors of the public episode table [T], one per paint. They are
screen approximations for labelling, **not measured paint colors**; for physical mixing use
pigment data. Pigment codes are the Colour Index pigment the generic name usually denotes;
products may use substitutes or hues. "Mixture" = a convenience name with no single pigment.

| paint | hex [T] | usual pigment | role and strength (cards) |
|---|---|---|---|
| Titanium White | #FFFFFF | PW6 | all lights; firm and dry for snow, thinned for water lines |
| Phthalo Blue | #0C0040 | PB15 | skies, water; very strong, a touch [S S12E13 1:31] |
| Prussian Blue | #021E44 | PB27 | darks, snow shadows; very strong [S S12E02 9:28] |
| Midnight Black | #000000 | mixture | darks; transparent over a glow [S S08E06 01:24] |
| Alizarin Crimson | #4E1500 | PR83 | sky warmth, lavender with blue; weak, so laid before blue with no wash [S S20E09 02:31] |
| Van Dyke Brown | #221B15 | mixture | earth, banks, trunks, every dark mix |
| Dark Sienna | #5F2E1F | mixture | warm earth, trunks with white |
| Burnt Umber | #8A3324 | PBr7 | occasional earth and trunks (9% of trunk steps [D]) |
| Sap Green | #0A3410 | mixture | greens, tree darks; left out in winter |
| Cadmium Yellow | #FFEC00 | PY35 (often a hue) | lit greens with sap green |
| Yellow Ochre | #C79B00 | PY43 / PY42 | duller warm highlights, grass |
| Indian Yellow | #FFB800 | mixture (hue) | warm glow, rich lit greens |
| Bright Red | #DB0000 | mixture | a touch in white [S S12E02 8:10]; opaque on a dark ground [S S08E13 19:29] |
| Phthalo Green | #102E3C | PG7 | occasional: water, evergreen darks |
| Liquid White / Clear | #FFFFFF | medium | base coat; Clear keeps darks dark where White would lighten them [S S10E10 09:35] |
| Liquid Black, Black Gesso | #000000 | medium / ground | dark base; transparent colors vanish on it [S S08E13 19:29] |

A painting uses 8–13 tubes, median 11 (`dataset/stats.md`).

## 3. Tools
| tool | stated | contact width | fraction of W | other dimensions |
|---|---|---|---|---|
| 2" brush | 2 in, flat [S name] | 2 in; face ≈ 2 in in a wide shot [M S12E02 07:16] | 0.083 | bristle length ≈ 1–1.2× width [M S11E01 01:35, ±30%]; corner contact ≈ 0.3–0.5 in [E] |
| 1" brush | 1 in, flat [S name] | 1 in; one stroke = 0.06 of portrait W = 1.1 in [M S17E07 12:22] | 0.042 | bristle length ≈ width [M S12E02 17:49]; chisel edge ≈ 0.1 in thick [E] |
| fan #6 | the usual fan [S S07E03 23:52, S05E01 03:58] | spread ≈ 1.5–2 in [M S08E06 20:50] | 0.06–0.08 | edge-on contact ≈ 0.1–0.2 in [E] |
| fan #3 | small fan [S S07E03 23:50, S15E01 15:35] | ≈ 1 in [E] | 0.04 | |
| filbert #6 | bristle filbert [S S09E06 10:15] | ≈ 0.4–0.6 in [E] | 0.02 | rounded tip |
| round | a big round brush [S S07E01 04:34] | head ≈ 1.5 in across [M S07E04 15:11] | 0.06 | |
| liner #2 | script liner [S S01E04 25:38, S11E09 11:46] | line 0.03–0.15 in [E] | 0.001–0.006 | hair ≈ 1 in [E]; thinned paint |
| large knife | the knife [S] | blade ≥ 3 in long beyond the hand, ≈ 1 in at the heel, tapering to a point [M S12E02 06:27] | edge up to 0.125 | roll on the edge ≈ 0.05–0.15 in [E] |
| small knife | for tight spots [M S11E01 10:43] | blade ≈ 1.5–2 in, narrow and pointed [E; seen S11E01 11:07, size not measurable] | 0.06–0.08 | |

Bristles bend under firm pressure and the mark widens [S S12E02 17:52, S17E07 12:22].

## 4. Stroke primitives
Width = contact width as a fraction of landscape W. Length in inches (fraction of W). Pressure on
the 0–1 scale of `01-materials.md`. Positions and lengths from the studies are [M] unless marked.

| stroke | tool, part | width | length | angle | pressure | repetitions, spacing | load |
|---|---|---|---|---|---|---|---|
| criss-cross | 2" flat | 0.083 | 2–4 in (0.08–0.17) [M S07E04, S11E01 01:21, S12E02 0:26, S15E08 0:21, S20E09] | alternating ±45 [M] | 0.2–0.6; firm in S11E01 [M] | rows from the top down, ~50% overlap [E] | a touch, tapped in evenly [S S20E09 02:43] |
| horizontal pull | 2" flat | 0.083 | sky: full width (1.0); water: edge to center, 0.3–0.5 [M S12E02 1:48] | 0 | 0.4–0.6, last pass 0.05 [M] | water rows from the bottom up [M S12E02 1:48] | same dirty brush |
| dry blend | clean dry 2" | 0.083 | full width | 0 or ±45 | 0.05–0.35 | 2–4 passes [E] | none, dry [S S12E02 5:01] |
| tiny circles | 1" corner (or fan) | 0.02–0.04 | bumps 0.5–1 in [M S19E13 02:37] | circular, always moving | 0.4–0.6 | continuous chain [M] | full of white |
| base blend | dry 1"/2" corner | 0.02 [E] | circles along the cloud base only | circular | 0.2–0.35 | one pass [M S11E01 06:15] | none |
| fluff | dry 2" corner | 0.02 [E] | lifts ≈ 0.3–0.5 in [E] | up and around, never −90 | 0.05–0.15 | many [M S11E01 07:04] | none |
| knife outline | knife long edge, roll | roll ≈ 0.005 [E] | ridges 0.2–0.65 of W [M S12E02 6:00] | far ridge 15–20; near 35–45 then flatter [M S19E13 05:04, 06:49]; blade nearly upright [M S12E02 6:00] | 0.9–1 [S S19E13 05:37] | lift and re-place per peak | small roll, dark mix |
| scrape | knife flat | blade | over the whole shape | any | 0.9–1 | until excess is gone [S S12E13 4:58] | clean |
| pull-down | 2" flat | 0.083 | ridge to mist line (base at y 0.45–0.6) [M S08E06 06:47, S12E02 7:16] | +90 or down the slope | 0.65 → 0.2 along the stroke [M] | side by side | paint already on the canvas |
| knife float | knife edge or tip, roll | roll only | 0.5–4 in (0.02–0.17) [M S11E01, S12E02 8:10, S12E10, S19E13 10:13] | slope angle 30–50 [M S01E06 07:11, S12E10 09:04, S19E13] | 0.05–0.15 [S S12E02 8:41] | many short strokes from the ridge down | firm, dry white [S S12E02 8:54] |
| opposing float | knife edge, roll | roll only | 1–2 in [M S19E13 12:53] | mirror of the float (180 − θ) | 0.05–0.2 | one per highlight, beside it | white + a little blue |
| tap and lift | dry 2" flat/corner | 0.083 | taps, lift ≈ 0.2 in [E] | taps follow the slope; lift −90 | 0.2–0.35 | spacing ≈ 0.5 in [E] | none |
| corner zigzag | 1" chisel corner / fan corner | swing 0.5 in at top → 2 in at bottom (0.02→0.08) [M S12E02 16:56] | tree 0.35–0.7 of H [M S12E02 16:56, 19:15] | swings ≈ 0 ± 20 [E]; leader +90 | 0.2 → 0.8 top to bottom [S S12E02 17:52] | swing step ≈ 0.2–0.3 in [E] | full, chisel reshaped per tree |
| push up | fan flat or 1" | 0.04–0.08 | ≈ 0.5 in per push [M S20E09] | −60 to −90 | 0.65–0.85 | rows from the top, each wider | full |
| tap down | fan edge vertical | 0.005–0.01 [E] | dab 0.3–0.8 in [E] | +90 | 0.2–0.35 | spacing 0.2–0.5 in [E] | dark, full |
| stamp / pounce | 2" or 1" face | 0.042–0.083 | no slide | n/a | 0.65–0.85 | repeated into a ragged mass [M S08E06 18:26] | dark, full |
| lift up | 1" flat | 0.042 | 0.3–0.5 in [M S19E13 16:07] | −90 | 0.2–0.35 | side by side | none (moves wet dark) |
| reflection | 2" flat | 0.083 | far shore 0.08–0.1 of H, near 0.2 of H [M S12E02 13:54, 21:05]; 1–2 in [M S12E10 14:21] | +90, then 0 | 0.2–0.35, then 0.05–0.15 [S S12E02 25:05] | one pull per clump, then 1–2 across | none |
| water line | knife long edge, Liquid White roll | roll ≈ 0.005 [E] | up to 0.5 of W [M S12E02 16:00]; ripples 0.5–2 in [M S12E13 15:57] | 0, dead level [S S12E02 16:41] | line 0.65–0.85; ripples 0.2–0.35 | one line, a few ripples | thin roll |
| cut / scratch | knife edge or tip | 0.001–0.004 [E] | trunk height | ≈ +90 [M S11E01 20:05] | 0.2–0.35 | few | clean or thin roll |
| knife slab | knife flat, roll | 0.02–0.04 | blocks 0.5–1 in [M S19E13 21:30] | one shared tilt per group [M S12E02 25:55] | 0.4–0.6 | short pushes | Van Dyke roll |
| skip and bounce | knife edge, tiny roll | roll only | 0.5–1.5 in [E] | along the rock angle | 0.05–0.15 | repeated touch-lift [M S17E07 14:00] | tiny roll |
| sheet pull | 1" flat | 0.045 (0.06 of portrait W) [M S17E07 12:22] | 0.25 of H [M S17E07 12:22] | +90, slight arc | 0.2–0.35, bristles bend | side by side, one brush width apart | Liquid Clear, then white; heavy at the top |
| liner pull | liner tip | 0.001–0.006 [E] | limbs 1–4 in [E] | outward from the trunk, wobbling | 0.2–0.35 | few per tree | thinned to flow [S S15E08 23:19] |

## 5. Wet-paint behaviour model
Rules a simulator must implement, with the evidence and a starting parameter.

| # | rule | evidence | suggested parameter [E] |
|---|---|---|---|
| 1 | **The wet base dilutes.** Paint laid into Liquid White mixes with it and lightens, more with distance from the start of the stroke; over Liquid Clear the color keeps its value | [S S10E10 09:35; M S12E02 0:26, S15E08 0:21] | deposit = mix(brush, base, α), α 0.3–0.6 on White, 0.05–0.15 on Clear; per-stroke reservoir decay ≈ 0.3 per inch |
| 2 | **The brush is a reservoir both ways.** It deposits and picks up; an unwashed brush carries the previous mix into the next step | [S S20E09 02:31; M S12E02 1:48, S12E10 01:15] | exchange rate 0.1–0.3 per contact; washing resets to empty |
| 3 | **Thin over thick.** A thinner, softer layer sticks on a thicker one; otherwise the strokes pick up and smear | [S S11E01 04:09, S01E06 10:28, S08E06 17:37, S11E03 13:38] | deposit efficiency = clamp(1 − k·(h_brush_viscosity − h_canvas_viscosity)), k ≈ 1 |
| 4 | **Highlights need firm, dry paint and no pressure**, or they turn to mud | [S S12E02 8:41, S15E08 3:30] | mud = mix with layer below when load viscosity < 0.5 or p > 0.3 |
| 5 | **A knife roll prints only its edge.** Contact is a line along the blade, the roll width wide | [M S11E01 07:53, S12E10 08:09; `01-materials.md` loading] | footprint = edge length × 0.05–0.15 in; flat of the blade never deposits |
| 6 | **Partial contact on the canvas tooth.** At whisper pressure paint catches only on the weave tops and leaves holes | [S S19E13 10:13, S12E02 8:41; M S12E02 8:10] | coverage = smoothstep(p, 0.05, 0.4) × tooth noise, period 0.02–0.05 in |
| 7 | **Scraping removes paint** and makes the next layer stick | [S S12E13 4:58, S19E13 07:42, S07E07 14:57, S08E13 05:13] | knife flat at p > 0.8 removes 60–90% of wet thickness |
| 8 | **A clean dry brush blends without adding paint**; it must be dry | [S S11E01 04:09, S12E02 5:01] | box-blur of color under the footprint along the path; strength ∝ 1 − p |
| 9 | **Colors mix on the canvas and on the tool**, unevenly; several colors loaded side by side stay marbled | [S S07E04 08:23, S17E07 14:31, S19E13 14:39] | load as 2–4 color bands across the bristles; no premixing |
| 10 | **Transparency**: blue, black and crimson vanish over a dark ground or let a glow show; bright red and white cover | [S S08E13 19:29, S08E06 01:24] | opacity: white 1.0, bright red 0.8, ochre 0.7, blues/black/crimson 0.2–0.4 |
| 11 | **Cutting exposes the ground**: a knife edge through wet dark paint shows the canvas or the layer below | [S S11E01 20:31] | remove wet layer along a 0.03–0.1 in line |
| 12 | **Pressure bends bristles and widens the mark** | [S S12E02 17:52] | width = w0 · (1 + 0.6p) for brushes; knife unchanged |
| 13 | **Reflections are a transform** of the wet paint already there: pulled straight down, then softened across | [S S12E02 14:06, 21:14] | copy-smear down by the reflection length, then horizontal blur at p 0.1 |

## 6. Painting program
From 379 regular episodes [D]:
- **Steps per painting**: median 34 (quartiles 31–38, range 13–58); 13,052 steps in total.
- **Time**: median 25.4 min from first to last painting step; one step lasts a median 38 s
  (quartiles 26–53 s). A step's duration is the gap to the next step, so it includes talk and
  cleaning.
- **Order**: mean start position per subject is in `dataset/stats.md` (sky 0.01, mountain 0.18,
  water 0.29, trees and bushes ≈ 0.5, grass 0.60, path 0.75).

| stage (subjects) | mean share of painting time [D] |
|---|---|
| sky (sky, cloud, sun/glow, moon) | 15% |
| background (mountain, snow, mist, far trees) | 20% |
| water (water, reflection, water line, stream, waterfall, ocean, beach) | 12% |
| trees (evergreen, leaf tree, trunk/limbs) | 24% |
| ground (bush, grass, land, rock, path, fence, flower) | 21% |
| structures | 4.5% (median 0: only 100 episodes have one) |
| other | 4% |

| subject (episodes) | median steps (quartiles) | median minutes [D] |
|---|---|---|
| ocean/wave (33) | 14 (9–15) | 9.5 |
| structure (100) | 6.5 (5–9) | 3.3 |
| mountain (192) | 6 (4–8) | 5.2 |
| leaf tree (275) | 4 (2–5) | 2.9 |
| trunk/limbs (322), snow (104), evergreen (176), bush (289), cloud (201) | 3 (2–5) | 2.1–2.5 |
| sky (333), water (234), land (264), far trees (255), grass (229), rock (159), reflection (184) | 2 (1–3) | 0.8–2.0 |
| mist (183), water line (189), path (108), waterfall (43) | 1 (1–2) | 0.7–1.2 |

### From one dataset step to a stroke call
`stroke(name, tool, part, path, width, pressure, load)`:

| step field | parameter | how |
|---|---|---|
| `t`, next `t` | schedule, time budget | order is binding (back to front); duration ≈ number of strokes |
| `subject` | layer and region | the region from the subject card and `04-composition.md` |
| `action`, `motion` | `name`, `path` | match to section 4 (criss, circle, pull down, tap, push up, zigzag, float); a dozen keywords cover about half of all steps [D]; else use the subject's default stroke |
| `tool` | tool model, `width` | section 3; `unknown` (16% [D]) → the subject's most common tool in `01-materials.md` |
| `part` | contact geometry | `unknown` (54% [D]) → the part in the stroke table |
| `paint` | `load.colors` | hex from section 2; empty list = clean dry brush or paint carried over (rule 2) |
| `load` | `load.amount`, thinned | full → 1.0, a touch or little → 0.1–0.2, dipped in Liquid White/Clear → thinned (rule 3) [E] |
| `pressure` | `pressure` | scale in `01-materials.md`; `unknown` in 22% [D]. Where given, the audit confirmed 38 of 39 against frames (`METHOD.md`); the stroke table gives frame-checked values |
| `where` | path anchor | words to fractions with `04-composition.md`; ±0.05 at best |
| `rule`, `new` | constraints | e.g. leave open spaces, keep the top edge sharp |
