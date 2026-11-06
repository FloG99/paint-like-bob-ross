# Painting order

Back to front, dark before light. Times are from the ~26-minute episodes and show the share of
effort.

## Canonical sequence
| # | step | ~time | notes |
|---|---|---|---|
| 0 | base coat (Liquid White/Clear) | before | thin, even, wet |
| 1 | sky color | 0:20–2:30 | criss-cross; leave holes for clouds |
| 2 | **water base, with the sky's brush** | 1:00–3:30 | lakes and streams get their blue now, before any land (before the mountain in 86/130, before the clouds in 69/134) |
| 3 | dry blend sky + water | 2:30–4:30 | light pressure; sky light at the horizon |
| 4 | clouds | 2:30–7:00 | farthest first; bodies, blend the bases, fluff the tops (before the mountain in 122/123) |
| 5 | far mountain(s) | 4:00–6:30 | knife outline, pull down, little detail |
| 6 | main mountain: dark | 5:00–9:30 | knife outline, scrape, pull-down, mist base |
| 7 | main mountain: snow and shadows | 6:00–12:30 | knife float on lit faces, opposing float for shadows |
| 8 | mist at the base | 11:00–13:00 | tap and lift along the angles |
| 9 | far tree line / far shore | 12:30–17:00 | fan tap down; dark first, a few highlights |
| 10 | reflections and the far water line | 14:00–17:00 | pull down, across; knife line (reflection before its water line in 125/146) |
| 11 | middle trees, banks, land | 17:00–21:00 | darks first: evergreens, pounced banks (evergreen before bush in 96/134) |
| 12 | highlights, grass, bushes | 21:00–25:00 | far to near, each plane lighter |
| 13 | rocks, near water lines, ripples | 19:00–26:00 | knife slabs, Liquid White lines |
| 14 | big framing tree, trunks, twigs, last highlights | 22:00–27:00 | the biggest dark goes in late, over everything |

## Measured order (all 379 episodes, `dataset/stats.md`)
Mean position of a subject's first step, 0 = start of the episode, 1 = end (the number of episodes that paint it in brackets):

| position | subjects |
|---|---|
| 0.0–0.15 | sky 0.01 (333), cloud 0.09 (201), sun/glow 0.11 (69) |
| 0.15–0.40 | mountain 0.18 (192), water 0.29 (233), mist 0.30 (183), far trees 0.30 (255), ocean 0.32 (33), snow 0.36 (101) |
| 0.40–0.55 | reflection 0.49 (184), waterfall 0.50, bush 0.50 (285), structure 0.50 (100), trunk/limbs 0.50 (315), leaf tree 0.50 (275), land 0.50 (264), evergreen 0.51 (172), stream 0.52 |
| 0.55–0.85 | water line 0.59 (189), grass 0.60 (227), rock 0.62 (158), path 0.74 (106), fence 0.79 (52), flower 0.84 (7) |

The table above holds on average: sky, clouds, mountain, water and far trees come first; reflections, land and trees in the middle; water lines, grass and rocks after them; paths and fences last.

**Pair rules, with counts** (episodes painting both; "A before B" = A's first step comes earlier):
- Clouds before the mountain: 122/123. The one fixed rule. Sky before cloud 184/191.
- Mountain before far trees 127/138; far trees before evergreen 112/130; evergreen before leaf tree 87/120.
- Reflection before its water line: 125/146 (85% weighted); the other 21 put the knife line first and pull the reflection under it.
- Evergreen before bush: 96/134 (71% weighted); in the other 38 the bush is laid first.
- Structure before path 44/47 and before fence 38/39; path before fence 17/21.
- Land before grass 123/172.

**Exceptions, real:**
- **Water before clouds is a coin flip**: 69/134 (51% weighted), so step 2 is a habit, not a rule. Water before the mountain is clearer: 86/130 (67% weighted), the mountain first in 44/130.
- Water does not always get its blue early: far trees before water 65/155.
- Mist before far trees 91/142, snow before far trees 36/82: both are placed by the scene, not by the table.
- Bush before grass 107/177, grass before rock 54/99, water line before rock 50/85: no preferred order; paint by distance.
- Structures come mid-painting (before bush in 21/79): the bushes are tapped around it afterwards, see `subjects/structures.md`.
- Trunks and limbs: the first trunk step is mid-painting (0.50), but the big framing tree still comes last in the long episodes (after every other tree).

## Variants
- **Stream as a slab**: the stream is the sky-blue slab from step 2. The land is tapped in around it, and the only later water work is white streaks. [S11E01]
- **Dark underpainting**: the whole lower ~40% is scrubbed dark first, then hills, trees, stream and grass go over it. The stream is just white streaks on the dark. [S15E08 7:29]
- **Glow first**: for sunsets and backlit skies, warm color goes in first, and the blue and black only go around and above it, never over it. [S08E06, S12E10]
- **Clear base**: on Liquid Clear the sky colors are transparent bands and black stays black. The sky colors are put in the water before any land. [S12E10]
- **Black gesso**: the darks are pre-painted off camera and only touched up. [S17E07]
- **Water before clouds**: common. The water is painted right after the sky color, with the same brush. [S07E04, S11E01, S12E02]

## Never
- A layer under a nearer layer it should cover (always far before near).
- Light before its dark.
- Blending with a wet brush.
- Detail in the far plane.
