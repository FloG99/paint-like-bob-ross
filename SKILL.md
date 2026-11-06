---
name: wet-on-wet
description: Plan, teach or simulate a wet-on-wet (alla prima) oil landscape painting in the style taught by Bob Ross on The Joy of Painting, from composition down to single strokes (tool, load, path, angle, pressure). Use when someone wants to paint like Bob Ross, needs step-by-step guidance or troubleshooting for a wet-on-wet oil painting, or drives a painting simulator or robot in this style.
---

# Wet-on-wet painting

Goal: turn a scene idea into a painting plan in this style, then into concrete strokes.

## Read order (token-cheap)
1. `reference/00-method.md`: always (one page).
2. `reference/05-order.md` and `reference/04-composition.md`: to lay out the scene.
3. Only the `reference/subjects/*.md` cards for elements in the scene.
4. `reference/02-strokes.md` and `reference/01-materials.md`: when you translate steps into tool motions.
5. `reference/06-troubleshooting.md`: when tutoring, after each stage, and whenever the learner's result looks wrong.
6. `reference/07-simulation.md`: when driving a simulator or robot (canvas units, paint colors, tool sizes, stroke parameters).
7. Only to check a detail:
   - `studies/` for the in-depth notes behind a card (search for the timestamp it cites);
   - `dataset/` for the steps of any episode.

## Planning a painting
1. **Pick the light side** (usually right) and the time of day. Then pick the base coat:
   - Liquid White by default;
   - Liquid Clear for transparent glowing skies;
   - a dark underpainting for dark scenes.
2. **Lay out the planes** with the proportions in `04-composition.md`: the focal point first, then the framing darks, the open center and the light path in.
3. **Order the steps** with `05-order.md`: back to front, water with the sky, darks before lights, the big framing dark late.
4. **For each step, write down**:
   - the tool and the part of it that touches;
   - the mix and how it's loaded;
   - the stroke name from `02-strokes.md`, with its path, angle and pressure;
   - where on the canvas it goes;
   - what must stay unpainted.
5. **Check against the laws**:
   - one light;
   - every highlight has a shadow;
   - strokes follow the angles;
   - mist between planes;
   - water level and recessed;
   - darks kept;
   - no detail far away.

## Translating to a simulation or robot
All numbers (canvas units, paint colors, tool sizes, stroke widths, lengths, angles, pressure) are in `reference/07-simulation.md`, each tagged with its source.
- **Coordinates** on the cards are fractions of the canvas (x right, y down). Pressure words map to 0–1 per `01-materials.md`.
- **The wet base matters**: colors lighten and blend into it, so aim darker than the target when laying sky and water. Thin layers stick on thick ones: later highlights need less pressure and thinned paint.
- **A knife roll prints only its edge**. Snow and highlights are a whisper touch that breaks on the canvas tooth, so model partial contact, not a solid fill.
- **Reflections are a transform of the wet paint already there** (pull straight down, then across), not a repainted mirror image.
- **Tolerance**: positions in the notes are ±0.05 of the canvas. Anything marked `(?)` was inferred.
- **Counts** `(N/M)` on the cards are episodes whose narration names a step: a lower bound on how often it is done. Use them to choose between variants, not to drop a rule.

## Worked example
A new scene planned with the steps above: **an autumn lake under a snowy peak, light from the right, landscape canvas.**
- **Light and base**: right side, daytime. Liquid White, thin and even.
- **Layout** (`04-composition.md`): sky y 0–0.42; focal peak summit at x 0.42, y 0.14; mist at y 0.44–0.52; far tree line and shore y 0.5–0.58; lake y 0.58–1 with a sheen channel in the center as the light path; banks left and right; one big framing evergreen at the left edge, autumn trees on the right bank.
- **Order** (`05-order.md`): sky, lake with the sky brush, clouds, mountain, snow, mist, far trees, reflections, water line, banks, trees and bushes, grass and near lines, framing tree last.

Coordinates are fractions of the canvas (x right, y down). "Open" = what must stay unpainted or untouched in that step.

| # | step | tool, part | mix, load | stroke: path, angle, pressure | where (x, y) | open | card |
|---|---|---|---|---|---|---|---|
| 1 | sky | 2" flat | a touch of alizarin tapped in; then phthalo + midnight black over it, no wash | criss-cross, row by row from the top, light–medium | x 0–1, y 0–0.42; blue strongest at the top corners | cloud holes x 0.6–0.85, y 0.06–0.2; a pale band above y 0.38 | sky-clouds: Sky 1–2 |
| 2 | lake base | same dirty 2", flat | what is left on it (phthalo + black) | horizontal pull from the left and right edges inward, bottom up, medium | x 0–1, y 0.58–1 | sheen channel x 0.42–0.58, narrow at the far shore, wider at the bottom | water: Lake 1 |
| 3 | blend | clean dry 2", flat | none | dry blend: long horizontals, from light toward dark, whisper–light; stop early | sky and lake | the sheen; the horizon band | sky-clouds: Sky 3 |
| 4 | cloud bodies | 1" corner | titanium white + a touch of bright red, pulled through, a lot | tiny circles, brush always moving, medium | x 0.6–0.85, y 0.06–0.2 | bare spots inside the cloud | sky-clouds: Cumulus 1 |
| 5 | cloud base, top | clean dry 2" corner | none | base blend on the bottom only, light; then fluff the top up and around, whisper | cloud bottoms, then tops | the top during the base blend | sky-clouds: Cumulus 2–3 |
| 6 | mountain dark | knife, long edge with a roll | midnight black + Prussian + Van Dyke + a touch of alizarin, spread flat, roll cut | knife outline, blade nearly upright, peak down both sides, hard; then scrape, knife flat, hard | summit x 0.42, y 0.14; range x 0.12–0.85, base y 0.52 | sky above the ridge | mountains: 1–2 |
| 7 | mountain body | 2" flat | none (the paint on the canvas) | pull-down from the ridge down the slopes, firm → light; horizontals at the base | inside the range | a crisp ridge | mountains: 3 |
| 8 | snow | knife, thin roll | firm dry titanium white + a touch of bright red | knife float down each slope at its angle, 0.5–3", whisper; all at one angle | right-facing faces, upper two-thirds | the dark between broken strokes; all left-facing faces | mountains: 4 |
| 9 | snow shadows | small knife, roll | white + a little Prussian (+ a touch of Van Dyke) | opposing float at the opposite angle, whisper, right beside each highlight | left-facing faces, valleys, under bumps | the lit faces | mountains: 5 |
| 10 | mist | clean dry 2" | none | tap and lift along the slope angles, light; never sweep across | mountain base, y 0.44–0.52 | the peaks | mountains: 7 |
| 11 | far tree line | fan, edge vertical, both sides full | mountain dark + white (blue-grey) | tap down, short vertical taps, light; a few taller ones; touch the base with white and lift up | x 0–1 in uneven groups, y 0.5–0.58 | mist above; no highlights | trees: Distant tree lines |
| 12 | reflection | 2" flat | none (same wet paint) | reflection: straight down ~0.08, light; then one or two horizontals, whisper | under the tree line, y 0.58–0.66 | the sheen channel | water: Reflections |
| 13 | far water line | knife, long edge, roll | Liquid White + a touch of alizarin | water line: one dead-level line, firm; two or three short ripples, light | y 0.58, x 0.1–0.9 | the rest of the lake | water: Water lines |
| 14 | banks | 2" flat | Van Dyke + the tree dark | stamp straight down, firm, ragged lower edges | left x 0–0.35, y 0.72–1; right x 0.62–1, y 0.66–1 | lake center x 0.35–0.62 | land: Land 1 |
| 15 | autumn trees, bushes | 1", pulled through in one direction; then 1" corner | dark: Prussian + Van Dyke + alizarin + sap green; lights: a touch of Liquid White, then yellow ochre, Indian yellow, a touch of bright red | push up dark masses, firm; then highlight clumps with less pressure on the right sides, limb by limb; stamp once straight down into the water under each shore bush | right bank x 0.62–0.95, y 0.5–0.75; a few bushes on the left bank | dark between clumps and on the left sides | trees: Leaf trees 1, 3; land: Bushes; 02-strokes |
| 16 | grass, near lines | fan or 2" flat; then knife | cadmium yellow + sap green + ochre + Indian yellow, mixed on the brush; then a Liquid White roll | taps down along the lay of the land, lit upper edges; then a dead-level water line at the foot of each bank | bank tops y 0.72–0.85; lines at each bank's foot | dark under the grass | land: Land 2; water: Water lines 5 |
| 17 | framing evergreen | fan corner, both sides full | mountain dark + sap green; then the dirty fan + cadmium yellow | leader down, then corner zigzag, wider and firmer toward the bottom; a few highlight dabs on the right edges, strongest at the top | left edge x 0.03–0.16, from off the top to y 0.95 | most of the tree stays dark | trees: Evergreens |
| 18 | trunks, twigs | clean knife edge; liner tip | dark sienna + white roll; thinned Van Dyke | cut through the wet dark, light; liner pull out from the trunk, light | inside the right-bank trees and bushes | — | trees: Trunks and limbs |

**Check**: one light (snow, leaves and tree highlights all on right-facing sides); every snow highlight has its shadow (step 9); strokes follow the slopes, water strokes level; mist between the peak and the tree line; water low and level with land above it; the framing tree and banks keep their darks; nothing detailed beyond the far tree line. After each stage, run the checklist in `reference/06-troubleshooting.md`.
