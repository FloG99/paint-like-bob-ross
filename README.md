# Wet-on-wet oil painting, step by step

*An independent study. Not affiliated with or endorsed by Bob Ross Inc.*

How to paint like Bob Ross: an evidence-based reference for wet-on-wet oil landscape painting, as
taught on the public-television series The Joy of Painting (1983–1994). Every rule cites the
episode and minute it comes from. It is written for people and for AI: painting tutors, AI agents
that guide you through a new painting, image generators, painting simulators and robot painters.

It has two parts:
- **A reference** with the rules of the technique, from composition down to the single stroke:
  which brush, which part of it, how much paint, which direction, how much pressure.
- **A dataset** with every painting step of 382 episodes, about 13,000 steps in total, as JSON.

## What it looks like
A rule from the trees card:

> **Load**: Use a fan loaded full on both sides (tool is a fan in 142/172) …
> [S12E02 16:56, S12E13 17:23, S11E01 13:51]

- `S11E01 13:51` is the evidence: season 11, episode 1, at 13:51.
- `142/172` is the support count: in 142 of the 172 episodes with evergreens, the narration names
  a fan brush. The counts include only what is said aloud, so they are lower bounds.

The same moment as a step in the dataset (`dataset/steps/S11E01.json`):

```json
{
 "t": "13:51",
 "subject": "evergreen",
 "action": "far evergreens with fan brush, dark mountain color",
 "tool": "fan",
 "part": "corner",
 "paint": ["midnight black", "van dyke brown", "alizarin crimson", "prussian blue", "sap green"],
 "load": "load the brush full of paint",
 "motion": "push them out",
 "pressure": "firm",
 "where": "way back in the distance"
}
```

## Use it with AI
The repository is a ready-made [agent skill](SKILL.md): it tells an AI assistant how to plan and
teach a painting in this style.
- **Claude Code and other agents that load skills:**
  `git clone https://github.com/FloG99/paint-like-bob-ross ~/.claude/skills/wet-on-wet`
- **Any chat assistant that reads files:** upload `SKILL.md` and the `reference/` folder.

Then ask, for example:
- *Guide me step by step through painting a snowy mountain lake in this style. I have the
  standard paints and brushes.*
- *Plan a sunset ocean painting, with the brush, color, stroke and position for each step.*
- *Here is a photo of my painting. Why do my clouds look flat, and how do I fix them?*
- *Turn this scene into stroke commands for my painting simulator.* (Uses `reference/07-simulation.md`.)

## Where to start
- **To learn the technique:** `reference/00-method.md` has the whole method on one page; then
  read the card for your subject in `reference/subjects/`.
- **To use the data:** `dataset/SCHEMA.md` explains the fields; `dataset/stats.md` has the totals.
- **To guide someone through a painting (tutor or agent):** `SKILL.md` (a standard agent skill,
  with a worked example), and `reference/06-troubleshooting.md` for what goes wrong.
- **To build a virtual painter, simulator or robot:** `reference/07-simulation.md` has the numbers:
  canvas, paint colors, tool sizes, stroke widths, lengths, angles and pressure.
- **To judge how reliable it is:** `METHOD.md`.

## What's inside
| folder | what |
|---|---|
| `reference/` | the method on one page, then materials, strokes, color, composition, painting order, troubleshooting, numbers for simulation, and one card per subject |
| `dataset/` | one JSON file per episode, the schema, and statistics |
| `studies/` | 16 episodes studied in depth, frame by frame. This is the evidence behind the cards |
| `SKILL.md` | how an agent uses all this to plan a painting |
| `METHOD.md` | sources, how it was made, how accurate it is, and its limits |

## How it was made
1. **Extraction:** every step of every episode is extracted from the captions and checked
   automatically: each timestamp must exist in that episode, the steps must run in order, and the
   episode must be complete.
2. **Deep study:** 16 episodes are studied against the video, frame by frame, for what the
   narration leaves out: angles, positions, pressure.
3. **Synthesis:** the cards are written from both and every rule is tested against the full dataset.

Language models did the extraction and drafting; their output was checked by code and by hand.
In a hand-checked audit against the frame-checked studies, the extraction invented no steps,
found 94% of the real ones, and 13.6% of steps had a wrong label. Details and limitations are in
`METHOD.md`.

## Coverage
- **Dataset:** 379 of the 381 regular episodes (the other 2 have no captions), plus 3 guest episodes
  that are marked and left out of the statistics.
- **Subjects with cards:** sky and clouds, mountains, water and reflections, streams and waterfalls,
  oceans, trees, land, bushes, rocks, paths and fences, structures, winter.
- **Thin spots:** subjects painted in few episodes. Each now has one frame-checked study, but the
  sample stays small: moons (named in 5 episodes), northern lights (2), flowers (8), deserts
  (3 with a cactus), oval formats (13 name the oval). Oceans (33) and structures (100) are common
  in the dataset but rest on one or three studies.

## Related work
Existing projects offer episode tables (two are used here as sources), galleries, quote
collections, neural style transfer and toy robot painters. None documents the technique step by
step with evidence, and none offers a per-step dataset.

## License
[CC BY 4.0](LICENSE): you can share and adapt this, also commercially, as long as you give credit,
for example "wet-on-wet by FloG99, github.com/FloG99/paint-like-bob-ross, CC BY 4.0".

The license covers this repository's own work only: the descriptions, the analysis and the dataset.
It does not cover the show, its broadcasts, or any right of their owners.

## Legal
- This is an independent, unofficial study of a painting technique, for education. It is not
  affiliated with or endorsed by Bob Ross Inc. or any other rights holder.
- "Bob Ross" and "The Joy of Painting" are trademarks of their respective owners. They are used here
  only to say what was studied.
- No video, frames, images or transcripts are included, and nothing is quoted. Everything is
  paraphrased in my own words, with timestamps as evidence.
- Paint names are ordinary pigment and product names.
