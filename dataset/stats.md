# Statistics

## Steps over 379 extracted episodes

Share of episodes in which a value occurs for a subject; `w` = the same share weighted by episode rating (weight 0.4–1.6, see METHOD.md). Generated from `dataset/steps/`. Guest-painter episodes (3: S04E11, S05E09, S07E05) are left out, as they show other methods.

### Order: mean position of a subject's first step (0 = start, 1 = end)

| subject | episodes | mean first position |
|---|---|---|
| sky | 333 | 0.01 |
| moon/stars | 3 | 0.05 |
| cloud | 201 | 0.09 |
| sun/glow | 69 | 0.11 |
| mountain | 192 | 0.18 |
| water | 234 | 0.29 |
| mist | 183 | 0.30 |
| far trees | 255 | 0.30 |
| ocean/wave | 33 | 0.32 |
| snow | 104 | 0.38 |
| reflection | 184 | 0.49 |
| waterfall | 43 | 0.50 |
| bush | 289 | 0.50 |
| structure | 100 | 0.50 |
| leaf tree | 275 | 0.50 |
| land | 264 | 0.50 |
| trunk/limbs | 322 | 0.50 |
| evergreen | 176 | 0.51 |
| stream | 26 | 0.52 |
| other | 249 | 0.53 |
| beach | 19 | 0.58 |
| water line | 189 | 0.59 |
| grass | 229 | 0.60 |
| rock | 159 | 0.62 |
| path | 108 | 0.75 |
| fence | 52 | 0.79 |
| flower | 8 | 0.83 |

### Which comes first

- water before cloud: 70/135 episodes (51% weighted)
- water before mountain: 87/131 episodes (67% weighted)
- mountain before cloud: 1/123 episodes (1% weighted)
- evergreen before bush: 100/138 episodes (72% weighted)
- reflection before water line: 125/146 episodes (85% weighted)

### Per subject: tools, parts, pressure, paints

#### trunk/limbs (322 episodes)
- tool: liner 64% (w 64%), knife 60% (w 63%), fan 34% (w 37%), 2in 11% (w 12%), 1in 3% (w 3%), filbert 3% (w 3%), small knife 2% (w 2%), round 2% (w 1%)
- part: tip 61% (w 76%), edge 40% (w 47%), flat 13% (w 16%), roll 6% (w 8%), corner 7% (w 8%), chisel 0% (w 0%)
- pressure: light 86% (w 98%), whisper 13% (w 15%), firm 12% (w 15%), medium 4% (w 4%)
- paint: van dyke brown 64% (w 69%), titanium white 62% (w 65%), dark sienna 36% (w 35%), midnight black 16% (w 16%), alizarin crimson 17% (w 16%), sap green 13% (w 12%), burnt umber 9% (w 12%), phthalo blue 11% (w 11%)

#### bush (289 episodes)
- tool: 1in 40% (w 46%), 2in 43% (w 43%), fan 29% (w 30%), round 12% (w 13%), knife 8% (w 10%), liner 6% (w 6%), other: oval brush 2% (w 1%), filbert 1% (w 1%)
- part: corner 32% (w 51%), flat 24% (w 42%), tip 13% (w 21%), edge 4% (w 8%), roll 0% (w 1%), chisel 0% (w 0%)
- pressure: light 81% (w 95%), firm 7% (w 9%), whisper 6% (w 8%), medium 3% (w 3%)
- paint: sap green 54% (w 54%), yellow ochre 51% (w 50%), bright red 34% (w 33%), titanium white 31% (w 31%), alizarin crimson 30% (w 28%), indian yellow 28% (w 28%), van dyke brown 24% (w 26%), cad yellow 23% (w 24%)

#### leaf tree (275 episodes)
- tool: 2in 42% (w 45%), fan 42% (w 43%), 1in 24% (w 27%), knife 14% (w 16%), round 15% (w 15%), liner 13% (w 14%), other: oval brush 3% (w 3%), filbert 3% (w 2%)
- part: corner 39% (w 59%), flat 25% (w 39%), tip 14% (w 21%), edge 10% (w 16%), chisel 3% (w 5%), roll 1% (w 1%)
- pressure: light 81% (w 90%), firm 17% (w 21%), whisper 10% (w 13%), medium 12% (w 12%), hard 1% (w 2%)
- paint: sap green 54% (w 59%), van dyke brown 53% (w 56%), yellow ochre 44% (w 45%), alizarin crimson 45% (w 45%), midnight black 35% (w 34%), titanium white 33% (w 33%), bright red 27% (w 25%), prussian blue 26% (w 25%)

#### sky (333 episodes)
- tool: 2in 68% (w 91%), 1in 4% (w 7%), fan 3% (w 5%), other: clean dry brush 3% (w 4%), knife 1% (w 2%), other: blender brush 1% (w 1%), other: mighty brush 0% (w 1%), other: dry brush 0% (w 1%)
- part: flat 34% (w 89%), corner 5% (w 12%), edge 1% (w 3%)
- pressure: light 80% (w 98%), whisper 16% (w 20%), firm 2% (w 3%)
- paint: phthalo blue 58% (w 57%), alizarin crimson 34% (w 34%), titanium white 26% (w 26%), prussian blue 23% (w 23%), midnight black 22% (w 22%), yellow ochre 21% (w 19%), indian yellow 14% (w 14%), bright red 12% (w 12%)

#### far trees (255 episodes)
- tool: fan 39% (w 46%), 2in 37% (w 37%), 1in 13% (w 17%), round 14% (w 15%), liner 7% (w 7%), knife 4% (w 4%), other: oval brush 2% (w 2%), other: foam brush 1% (w 1%)
- part: corner 23% (w 42%), flat 18% (w 35%), tip 15% (w 28%), edge 2% (w 4%), chisel 2% (w 3%)
- pressure: light 79% (w 92%), whisper 11% (w 12%), firm 5% (w 5%), medium 1% (w 1%)
- paint: alizarin crimson 46% (w 50%), sap green 38% (w 45%), van dyke brown 36% (w 44%), midnight black 31% (w 35%), prussian blue 31% (w 35%), titanium white 31% (w 34%), phthalo blue 27% (w 28%), yellow ochre 18% (w 21%)

#### land (263 episodes)
- tool: knife 41% (w 47%), 2in 38% (w 43%), fan 34% (w 42%), 1in 8% (w 10%), round 4% (w 4%), liner 1% (w 1%), filbert 2% (w 1%), small knife 1% (w 1%)
- part: flat 28% (w 51%), edge 26% (w 47%), roll 9% (w 19%), corner 4% (w 8%), tip 1% (w 1%)
- pressure: light 72% (w 88%), whisper 15% (w 19%), firm 10% (w 13%), medium 8% (w 8%), hard 0% (w 0%)
- paint: van dyke brown 63% (w 70%), titanium white 51% (w 53%), sap green 32% (w 34%), dark sienna 29% (w 29%), alizarin crimson 26% (w 25%), yellow ochre 19% (w 22%), phthalo blue 16% (w 18%), prussian blue 16% (w 17%)

#### other (245 episodes)
- tool: liner 38% (w 47%), 2in 28% (w 33%), fan 27% (w 33%), knife 15% (w 21%), filbert 4% (w 4%), 1in 3% (w 3%), small knife 2% (w 3%), hand 2% (w 2%)
- part: tip 31% (w 55%), flat 18% (w 33%), edge 9% (w 19%), corner 7% (w 10%), roll 0% (w 1%)
- pressure: light 81% (w 95%), whisper 8% (w 11%), firm 7% (w 8%), medium 2% (w 3%), hard 0% (w 1%)
- paint: bright red 36% (w 36%), titanium white 27% (w 28%), van dyke brown 24% (w 28%), alizarin crimson 24% (w 24%), sap green 20% (w 20%), prussian blue 15% (w 16%), midnight black 15% (w 15%), permanent red 10% (w 14%)

#### grass (227 episodes)
- tool: fan 48% (w 57%), 2in 39% (w 44%), 1in 8% (w 9%), liner 8% (w 8%), knife 6% (w 7%), round 2% (w 2%), small knife 1% (w 2%), other: oval brush 1% (w 1%)
- part: flat 21% (w 53%), corner 11% (w 29%), tip 11% (w 25%), edge 4% (w 11%), chisel 0% (w 1%)
- pressure: light 78% (w 95%), whisper 5% (w 7%), firm 4% (w 4%), medium 2% (w 2%), hard 0% (w 1%)
- paint: sap green 55% (w 63%), yellow ochre 53% (w 60%), indian yellow 30% (w 33%), cad yellow 26% (w 30%), bright red 24% (w 24%), titanium white 17% (w 19%), cadmium yellow 16% (w 18%), van dyke brown 16% (w 17%)

#### water (233 episodes)
- tool: 2in 56% (w 65%), fan 27% (w 30%), knife 16% (w 20%), liner 5% (w 5%), small knife 4% (w 4%), 1in 2% (w 3%), other: clean brush 2% (w 2%), filbert 1% (w 1%)
- part: flat 30% (w 68%), edge 13% (w 30%), tip 5% (w 8%), corner 3% (w 7%), roll 1% (w 3%)
- pressure: light 79% (w 93%), whisper 10% (w 12%), firm 4% (w 4%), hard 2% (w 3%), medium 1% (w 2%)
- paint: phthalo blue 51% (w 51%), titanium white 45% (w 47%), midnight black 19% (w 20%), prussian blue 18% (w 20%), alizarin crimson 17% (w 18%), phthalo green 16% (w 17%), van dyke brown 10% (w 13%), liquid white 11% (w 10%)

#### mountain (192 episodes)
- tool: 2in 82% (w 82%), knife 69% (w 69%), small knife 17% (w 17%), fan 17% (w 16%), 1in 6% (w 6%), other: oval brush 2% (w 3%), round 3% (w 2%), other: clean dry brush 2% (w 2%)
- part: edge 53% (w 62%), flat 51% (w 58%), roll 18% (w 23%), corner 19% (w 22%), tip 7% (w 7%), chisel 1% (w 1%)
- pressure: light 92% (w 95%), firm 44% (w 45%), whisper 44% (w 44%), medium 10% (w 9%), hard 8% (w 9%)
- paint: titanium white 85% (w 85%), alizarin crimson 74% (w 73%), van dyke brown 54% (w 56%), prussian blue 55% (w 54%), midnight black 53% (w 50%), phthalo blue 51% (w 48%), sap green 24% (w 24%), dark sienna 20% (w 20%)

#### cloud (201 episodes)
- tool: 2in 74% (w 79%), fan 37% (w 40%), 1in 20% (w 22%), knife 6% (w 8%), other: blender brush 5% (w 5%), other: clean dry brush 2% (w 3%), other: clean brush 1% (w 2%), round 1% (w 2%)
- part: corner 46% (w 68%), flat 35% (w 51%), edge 3% (w 6%), tip 4% (w 5%), roll 0% (w 1%)
- pressure: light 92% (w 96%), whisper 33% (w 34%), firm 4% (w 5%), medium 4% (w 5%), hard 1% (w 1%)
- paint: titanium white 79% (w 83%), alizarin crimson 25% (w 24%), phthalo blue 24% (w 23%), bright red 21% (w 22%), midnight black 17% (w 17%), permanent red 7% (w 10%), prussian blue 8% (w 9%), van dyke brown 5% (w 7%)

#### evergreen (176 episodes)
- tool: fan 82% (w 85%), 2in 18% (w 19%), 1in 9% (w 10%), knife 6% (w 6%), other: oval brush 5% (w 4%), round 1% (w 1%), filbert 1% (w 1%), other: brush 1% (w 1%)
- part: corner 49% (w 75%), flat 15% (w 22%), chisel 7% (w 12%), tip 7% (w 10%), edge 3% (w 6%), roll 1% (w 2%)
- pressure: light 78% (w 89%), firm 22% (w 25%), medium 15% (w 15%), whisper 5% (w 6%), hard 3% (w 5%)
- paint: prussian blue 59% (w 60%), alizarin crimson 57% (w 59%), van dyke brown 53% (w 57%), midnight black 56% (w 54%), sap green 47% (w 50%), titanium white 33% (w 34%), phthalo blue 27% (w 28%), yellow ochre 18% (w 17%)

#### water line (188 episodes)
- tool: knife 72% (w 81%), fan 11% (w 12%), 2in 10% (w 11%), small knife 4% (w 4%), liner 4% (w 4%), round 2% (w 2%), other: clean brush 1% (w 1%), other: blender brush 1% (w 1%)
- part: edge 57% (w 80%), flat 12% (w 16%), roll 6% (w 9%), tip 3% (w 3%)
- pressure: light 62% (w 81%), firm 12% (w 16%), whisper 6% (w 9%), medium 3% (w 3%), hard 2% (w 2%)
- paint: liquid white 43% (w 46%), titanium white 31% (w 34%), magic white 12% (w 16%), phthalo blue 15% (w 16%), van dyke brown 11% (w 13%), bright red 7% (w 7%), alizarin crimson 6% (w 6%), prussian blue 4% (w 5%)

#### reflection (182 episodes)
- tool: 2in 59% (w 69%), fan 24% (w 29%), 1in 12% (w 15%), knife 8% (w 10%), round 7% (w 7%), other: clean brush 2% (w 3%), small knife 1% (w 1%), liner 1% (w 1%)
- part: flat 32% (w 84%), edge 5% (w 11%), corner 2% (w 6%), tip 2% (w 6%), roll 1% (w 2%)
- pressure: light 81% (w 91%), whisper 19% (w 22%), firm 3% (w 3%), medium 2% (w 1%), hard 1% (w 1%)
- paint: titanium white 26% (w 41%), prussian blue 17% (w 30%), van dyke brown 16% (w 30%), alizarin crimson 16% (w 26%), midnight black 14% (w 23%), phthalo blue 14% (w 21%), sap green 13% (w 21%), yellow ochre 5% (w 10%)

#### mist (182 episodes)
- tool: 2in 73% (w 84%), fan 7% (w 9%), other: clean dry brush 4% (w 5%), knife 4% (w 5%), round 3% (w 3%), other: clean brush 3% (w 3%), 1in 2% (w 2%), other: blender brush 1% (w 1%)
- part: flat 36% (w 78%), corner 11% (w 20%), tip 3% (w 5%), edge 1% (w 3%)
- pressure: light 72% (w 76%), whisper 24% (w 24%), firm 19% (w 17%), hard 1% (w 1%), medium 1% (w 1%)
- paint: titanium white 25% (w 79%), phthalo blue 5% (w 19%), magic white 2% (w 9%), midnight black 2% (w 7%), prussian blue 2% (w 6%), liquid white 2% (w 6%), yellow ochre 2% (w 5%), alizarin crimson 1% (w 3%)

#### rock (159 episodes)
- tool: knife 39% (w 43%), fan 31% (w 38%), filbert 23% (w 20%), small knife 12% (w 14%), 2in 9% (w 10%), liner 9% (w 9%), other: oval brush 4% (w 5%), 1in 4% (w 5%)
- part: edge 33% (w 59%), flat 19% (w 32%), tip 15% (w 25%), roll 4% (w 8%), corner 3% (w 5%)
- pressure: light 75% (w 89%), whisper 23% (w 28%), firm 4% (w 5%), medium 3% (w 3%)
- paint: titanium white 70% (w 72%), van dyke brown 69% (w 71%), dark sienna 40% (w 37%), midnight black 26% (w 25%), yellow ochre 14% (w 16%), phthalo blue 14% (w 15%), alizarin crimson 15% (w 14%), burnt umber 9% (w 12%)

#### structure (100 episodes)
- tool: knife 91% (w 91%), small knife 36% (w 35%), 2in 13% (w 13%), liner 8% (w 9%), fan 7% (w 7%), 1in 5% (w 5%), other: dry brush 1% (w 1%), other: old brush 1% (w 1%)
- part: edge 74% (w 91%), tip 22% (w 28%), flat 22% (w 25%), roll 14% (w 16%), chisel 2% (w 4%), corner 1% (w 1%)
- pressure: light 80% (w 91%), whisper 32% (w 39%), firm 28% (w 30%), medium 10% (w 11%), hard 2% (w 2%)
- paint: titanium white 95% (w 95%), van dyke brown 89% (w 89%), dark sienna 68% (w 64%), bright red 29% (w 26%), midnight black 25% (w 22%), yellow ochre 19% (w 16%), alizarin crimson 17% (w 15%), phthalo blue 15% (w 14%)

#### snow (104 episodes)
- tool: knife 51% (w 57%), 2in 51% (w 51%), fan 37% (w 38%), liner 15% (w 17%), 1in 7% (w 7%), round 5% (w 5%), small knife 4% (w 4%), other: blender brush 3% (w 3%)
- part: edge 32% (w 48%), flat 36% (w 47%), tip 12% (w 17%), roll 6% (w 10%), corner 4% (w 6%), chisel 4% (w 5%)
- pressure: light 75% (w 81%), whisper 28% (w 35%), firm 10% (w 11%), medium 2% (w 2%)
- paint: titanium white 98% (w 98%), phthalo blue 30% (w 29%), liquid white 20% (w 21%), prussian blue 15% (w 14%), alizarin crimson 13% (w 13%), bright red 12% (w 12%), van dyke brown 10% (w 11%), midnight black 9% (w 8%)

#### path (107 episodes)
- tool: fan 41% (w 48%), knife 28% (w 33%), 1in 7% (w 9%), 2in 8% (w 9%), small knife 6% (w 7%), other: oval brush 1% (w 2%), other: foam brush 1% (w 2%), round 1% (w 1%)
- part: flat 26% (w 51%), edge 16% (w 34%), roll 4% (w 8%), corner 4% (w 7%), tip 4% (w 7%)
- pressure: light 73% (w 85%), whisper 24% (w 30%), firm 4% (w 4%), medium 3% (w 2%)
- paint: titanium white 64% (w 71%), van dyke brown 64% (w 70%), dark sienna 32% (w 35%), prussian blue 8% (w 10%), alizarin crimson 11% (w 9%), phthalo blue 9% (w 8%), sap green 7% (w 7%), midnight black 6% (w 6%)

#### sun/glow (69 episodes)
- tool: 2in 55% (w 56%), knife 22% (w 27%), 1in 17% (w 23%), hand 13% (w 12%), other: finger 12% (w 12%), fan 10% (w 10%), other: blender brush 4% (w 5%), other: mighty brush 1% (w 2%)
- part: flat 28% (w 51%), edge 13% (w 29%), corner 13% (w 22%), tip 4% (w 5%)
- pressure: light 72% (w 84%), whisper 22% (w 27%), firm 10% (w 15%), hard 3% (w 4%)
- paint: titanium white 74% (w 71%), cadmium yellow 19% (w 20%), bright red 16% (w 18%), cad yellow 14% (w 17%), yellow ochre 19% (w 16%), indian yellow 13% (w 12%), alizarin crimson 12% (w 9%), permanent red 6% (w 8%)

#### fence (52 episodes)
- tool: liner 40% (w 46%), knife 33% (w 41%), small knife 10% (w 12%), filbert 12% (w 11%), fan 8% (w 10%), 1in 8% (w 9%), round 4% (w 5%), other: clean brush 2% (w 4%)
- part: tip 29% (w 51%), edge 25% (w 46%), heel 10% (w 16%), flat 4% (w 9%), corner 2% (w 3%)
- pressure: light 77% (w 92%), whisper 10% (w 14%), hard 2% (w 2%), firm 2% (w 2%)
- paint: van dyke brown 71% (w 74%), titanium white 60% (w 63%), dark sienna 13% (w 13%), liquid white 12% (w 12%), prussian blue 8% (w 10%), midnight black 8% (w 9%), sap green 10% (w 8%), bright red 6% (w 7%)

#### waterfall (43 episodes)
- tool: fan 67% (w 78%), 2in 19% (w 22%), other: oval 2% (w 5%), knife 5% (w 5%), 1in 5% (w 4%), liner 5% (w 3%), other: blender 2% (w 2%), filbert 2% (w 2%)
- part: flat 28% (w 77%), corner 7% (w 19%), edge 2% (w 6%), tip 2% (w 4%)
- pressure: light 74% (w 92%), firm 7% (w 11%), whisper 5% (w 7%), medium 2% (w 3%)
- paint: titanium white 84% (w 92%), phthalo blue 53% (w 50%), liquid white 26% (w 31%), magic white 7% (w 12%), liquid clear 9% (w 9%), prussian blue 7% (w 9%), phthalo green 7% (w 8%), van dyke brown 5% (w 6%)

#### ocean/wave (33 episodes)
- tool: fan 94% (w 97%), liner 73% (w 71%), 2in 61% (w 67%), filbert 64% (w 66%), small knife 27% (w 25%), knife 18% (w 20%), other: clean dry brush 3% (w 4%), 1in 3% (w 3%)
- part: corner 45% (w 55%), flat 42% (w 51%), tip 48% (w 51%), edge 24% (w 28%), roll 6% (w 6%)
- pressure: light 100% (w 100%), whisper 64% (w 67%), firm 48% (w 47%), hard 21% (w 20%), medium 18% (w 19%)
- paint: titanium white 97% (w 96%), phthalo blue 76% (w 73%), alizarin crimson 76% (w 72%), cad yellow 45% (w 46%), cadmium yellow 27% (w 29%), phthalo green 18% (w 17%), magic white 12% (w 15%), midnight black 12% (w 12%)

#### stream (26 episodes)
- tool: fan 62% (w 84%), 2in 12% (w 16%), knife 8% (w 12%), 1in 4% (w 8%)
- part: flat 19% (w 75%), corner 4% (w 15%), edge 4% (w 10%), tip 4% (w 10%)
- pressure: light 73% (w 100%), medium 4% (w 5%)
- paint: titanium white 77% (w 82%), phthalo blue 42% (w 41%), magic white 19% (w 32%), liquid white 27% (w 25%), prussian blue 19% (w 21%), alizarin crimson 15% (w 18%), midnight black 15% (w 15%), thalo green 4% (w 7%)

#### beach (19 episodes)
- tool: fan 47% (w 50%), knife 26% (w 34%), 2in 16% (w 15%), other: clean dry brush 5% (w 7%), other: second brush 5% (w 7%), other: brush 5% (w 5%), small knife 5% (w 4%)
- part: flat 37% (w 83%), edge 16% (w 43%), tip 5% (w 9%)
- pressure: light 95% (w 100%), whisper 16% (w 18%), firm 11% (w 9%)
- paint: titanium white 74% (w 80%), van dyke brown 47% (w 53%), dark sienna 37% (w 43%), yellow ochre 21% (w 23%), alizarin crimson 11% (w 14%), cad yellow 11% (w 10%), cadmium yellow 5% (w 8%), magic white 5% (w 7%)

#### flower (8 episodes)
- tool: 1in 62% (w 75%), filbert 12% (w 14%), 2in 12% (w 11%)
- part: tip 50% (w 85%), flat 12% (w 15%)
- pressure: light 100% (w 100%)
- paint: bright red 88% (w 88%), yellow ochre 38% (w 33%), indian yellow 38% (w 33%), titanium white 12% (w 12%), phthalo blue 12% (w 12%), liquid white 12% (w 10%), yellow 12% (w 10%), sap green 12% (w 9%)

#### moon/stars (3 episodes)
- tool: 2in 67% (w 67%), knife 33% (w 35%), other: finger 33% (w 33%), hand 33% (w 32%)
- part: edge 33% (w 100%), flat 33% (w 100%)
- pressure: light 100% (w 100%), firm 33% (w 35%)
- paint: titanium white 67% (w 100%), black 33% (w 48%)

---

## Paints and scene elements over all 403 episodes

Sources: per-episode color lists (see METHOD.md) and per-episode element tags (FiveThirtyEight). Counts are episodes.

### Paint usage
| paint | episodes | share |
|---|---|---|
| Titanium White | 400 | 99% |
| Alizarin Crimson | 380 | 94% |
| Van Dyke Brown | 371 | 92% |
| Cadmium Yellow | 346 | 86% |
| Yellow Ochre | 327 | 81% |
| Phthalo Blue | 323 | 80% |
| Bright Red | 321 | 80% |
| Midnight Black | 317 | 79% |
| Sap Green | 306 | 76% |
| Indian Yellow | 293 | 73% |
| Dark Sienna | 290 | 72% |
| Prussian Blue | 263 | 65% |
| Phthalo Green | 116 | 29% |
| Black Gesso | 114 | 28% |
| Burnt Umber | 55 | 14% |
| Liquid Clear | 51 | 13% |
| Liquid Black | 19 | 5% |
| Indian Red | 0 | 0% |

Colors per painting: median 11, range 1–15.

### Elements (share of episodes)

tree 90%, trees 84%, deciduous 56%, conifer 53%, clouds 44%, mountain 40%, lake 35%, grass 35%, river 31%, bushes 30%, snowy mountain 27%, mountains 25%, cumulus 21%, structure 21%, rocks 19%, snow 19%, cabin 17%, winter 17%, path 12%, sun 10%, waterfall 10%, ocean 9%, waves 8%, cirrus 7%, beach 7%, fence 6%, fog 6%, hills 4%, barn 4%

**With mountain** (160 episodes): tree 98%, trees 92%, conifer 81%, snowy mountain 68%, mountains 61%, clouds 54%, lake 51%, deciduous 42%, bushes 39%, grass 38%
**With river** (126 episodes): tree 100%, trees 96%, deciduous 66%, conifer 54%, grass 48%, clouds 40%, mountain 39%, bushes 36%, rocks 29%, waterfall 27%
**With waterfall** (39 episodes): tree 100%, trees 90%, river 87%, deciduous 59%, conifer 51%, grass 44%, bushes 38%, mountain 38%, rocks 38%, clouds 33%
**With snow** (75 episodes): tree 100%, trees 93%, winter 89%, conifer 75%, deciduous 53%, structure 44%, clouds 43%, mountain 39%, cabin 37%, lake 33%
**With cabin** (69 episodes): tree 100%, trees 93%, structure 87%, conifer 72%, deciduous 64%, clouds 43%, winter 42%, snow 41%, lake 36%, mountain 33%
**With lake** (143 episodes): tree 99%, trees 94%, conifer 64%, deciduous 58%, mountain 57%, clouds 43%, snowy mountain 41%, bushes 38%, mountains 36%, grass 31%

### Paint use by subject (share of those episodes)
| subject | n | most distinctive vs. all |
|---|---|---|
| mountain | 160 | Prussian Blue 81% (+16%), Black Gesso 16% (-13%), Phthalo Green 36% (+7%), Sap Green 82% (+6%) |
| snowy mountain | 109 | Prussian Blue 84% (+19%), Black Gesso 13% (-15%), Phthalo Green 39% (+10%), Yellow Ochre 75% (-6%) |
| river | 126 | Indian Yellow 86% (+13%), Sap Green 88% (+12%), Yellow Ochre 90% (+9%), Dark Sienna 80% (+8%) |
| waterfall | 39 | Black Gesso 54% (+26%), Sap Green 97% (+22%), Indian Yellow 92% (+20%), Yellow Ochre 95% (+14%) |
| winter | 69 | Sap Green 20% (-56%), Indian Yellow 28% (-45%), Cadmium Yellow 45% (-41%), Yellow Ochre 41% (-41%) |
| night | 11 | Indian Yellow 18% (-55%), Black Gesso 82% (+54%), Yellow Ochre 36% (-45%), Bright Red 36% (-43%) |
| lake | 143 | Prussian Blue 78% (+12%), Black Gesso 19% (-9%), Midnight Black 71% (-8%), Dark Sienna 66% (-6%) |
| deciduous | 227 | Sap Green 84% (+8%), Bright Red 85% (+6%), Indian Yellow 78% (+5%), Phthalo Green 24% (-5%) |

