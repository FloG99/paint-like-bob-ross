# Dataset schema

`dataset/steps/<EP>.json`: one file per episode, every painting action as one step, in order.
Extracted from the episode's captions (model: Claude Haiku; method and measured accuracy in
`METHOD.md`). `unknown` means the narration doesn't say it.

**How reliable each field is:**
- **From the narration:** `t`, `subject`, `action`, `paint`, `motion`, `where`, `rule`. Labels can
  still be wrong; the measured error rates are in `METHOD.md`.
- **Often unknown:** `tool` (16% of all steps), `part` (54%) and `pressure` (22%), because the
  narration often doesn't say them. Where a value is given it is usually right: in the audit,
  38 of 39 pressure values were confirmed by the video frames. For frame-checked tool, part and
  pressure, use `studies/`.

| field | type | meaning |
|---|---|---|
| `ep` | string | `SxxExx` |
| `base` | string | base coat: liquid white, liquid clear, liquid black, black gesso, other |
| `format` | string | landscape, portrait, oval, unknown |
| `light` | string | light side if stated: left, right, behind, unknown |
| `guest` | bool | a guest painter paints this episode (other methods; left out of `stats.md`) |
| `palette` | string[] | paints named in the episode |
| `steps[].t` | `mm:ss` | start of the step (±20 s) |
| `steps[].subject` | enum | sky, cloud, mountain, snow, water, reflection, water line, stream, waterfall, mist, sun/glow, moon/stars, far trees, evergreen, leaf tree, trunk/limbs, bush, grass, land, rock, path, structure, ocean/wave, beach, flower, fence, frame, `other: …` |
| `steps[].action` | string | short verb phrase |
| `steps[].tool` | enum | 2in, 1in, fan, knife, small knife, liner, round, filbert, sponge, towel, hand, `other: …`, unknown |
| `steps[].part` | enum | flat, corner, edge, chisel, tip, heel, long edge, roll, unknown |
| `steps[].paint` | string[] | paints on the tool for this step (empty = clean/dry tool or carried over) |
| `steps[].load` | string | how the tool is loaded, in plain words |
| `steps[].motion` | string | path and direction, in plain words |
| `steps[].pressure` | enum | whisper, light, medium, firm, hard, unknown (scale in `reference/01-materials.md`); see reliability above |
| `steps[].where` | string | placement if stated |
| `steps[].rule` | string | the stated reason, paraphrased (≤15 words) |
| `steps[].new` | string | anything unusual in this step |
| `rules` | string[] | general rules with `[mm:ss]` |

Episode metadata (title, colors, element tags) is in the two public episode tables listed in
`METHOD.md`; join on season and episode. Statistics over the steps are in `dataset/stats.md`.
