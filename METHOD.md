# Method

How this reference and dataset were made, how accurate they are, and where they fall short.

## In short
1. **Extraction:** language models turn each episode's captions into a list of painting steps.
   Code checks every file; an episode that fails is redone.
2. **Deep study:** 16 episodes are studied against the video, frame by frame.
3. **Synthesis:** the reference cards are written from the deep studies and tested against all
   382 episodes.

## Sources
- **Episode tables** for all 403 episodes, from two public datasets:
  - paint colors per episode: github.com/jwilber/Bob_Ross_Paintings;
  - scene elements per episode (mountain, river, cabin and so on): github.com/fivethirtyeight/data
    (bob-ross folder).
- **Ratings**, used only to set the processing order and the weights in `dataset/stats.md`:
  - IMDb episode ratings, from IMDb's official non-commercial dataset, as a Bayesian average;
  - YouTube like counts of the official uploads.

  Both are noisy and biased (IMDb favors season 1), so they are standardized and combined.
- **The episodes**, from the official public uploads. Captions and frames were studied locally and
  are not part of this repository.

## Step dataset (`dataset/steps/`)
1. Each episode's captions are read as a whole.
2. Every painting action becomes one step with fixed fields (see `dataset/SCHEMA.md`). Steps are
   described in neutral words; stated reasons are paraphrased; nothing is quoted.
3. **Checks**, run on every file:
   - **Timestamps:** every step's time must be one of that episode's own caption times.
     - Off by 5 seconds or less: the time is corrected to the nearest caption.
     - Off by more: the step is dropped, because it came from another episode (several episodes
       were processed per model call).
     - More than 10% dropped: the episode fails.
   - **Order and completeness:** steps must run in order, and the last step must be within
     3 minutes of the episode's end.
   - **Vocabulary:** tool, subject, part, pressure and paint values are mapped to the schema's
     fixed lists. A pressure value that names no pressure (a motion or a place) becomes
     `unknown`; it moves to `motion` when that is empty (177 steps). A paint is kept only if the
     episode names it.
   - **Wording:** the show's signature phrases are rewritten in neutral words.

   An episode that fails is redone and is never published. Over the full run, 3 episodes failed
   and were redone, 2 were stored under each other's names and swapped back, 12 steps were dropped
   and 25 timestamps corrected.
4. **Order:** episodes were processed best-rated first. After every four, one episode with an
   under-covered subject was added.
5. **Guest episodes:** 22 episodes are painted by guest painters using other methods. Three were
   extracted before this was noticed. They are kept with `"guest": true` and left out of the
   statistics. The others were not extracted.

## Accuracy of the dataset
The dataset was compared with the frame-checked deep-study notes of the same episodes, counted by
hand (±2). A step counts as found if the same action appears within about 45 seconds.

| measure | final pipeline (S07E04, S12E02, S17E07, S20E09) | first version (S08E06, S11E01, S15E08) |
|---|---|---|
| real painting steps found (recall) | 104 of 111 (93.7%) | 68 of 69 (98.6%) |
| invented steps | 0 of 147 | 0 of 135 |
| steps with a wrong field | 13.6% | about 35% |
| wrong subject / tool / part / paint | 6.1% / 3.4% / 2.0% / 1.4% | 13% / 11% / – / 11% |
| wrong motion | 0% | 0% |
| pressure, where given | 38 of 39 confirmed by the frames | – |
| field left `unknown`: tool / part / pressure | 30% / 66% / 55% | – |

**What this means:**
- **The steps are reliable.** No step was invented. The few missed steps are short sub-actions
  merged into a neighbouring step (a rock blend, a stone on a waterfall lip, a final highlight).
- **The labels are mostly right.** The remaining slips are mostly subjects: a conifer filed as a
  leaf tree, or a path entered as "other". The converter now maps such labels automatically.
- **Tool, part and pressure are often `unknown`**, because the narration rarely says them. Where
  a value is given, it is almost always right. The deep studies fill these fields in from video.

The first audit led to stricter extraction rules and the vocabulary checks above; the second
audit measures the published dataset.

## Deep study (`studies/`)
1. The narration is read first, and every change of step is marked.
2. Video frames are checked wherever the words leave something open: angle, direction, size,
   placement, amount of paint, result.
3. Inferences are marked `(?)`.
4. Positions are fractions of the canvas, accurate to about ±0.05.

## Reference cards (`reference/`)
- **Admission:** a rule goes into a card only if it is stated in an episode or seen in the deep
  studies. Every rule cites its evidence as `SxxExx mm:ss`.
- **Variants:** where episodes differ, the variants are listed side by side. Better-rated episodes
  set the default and come first as examples.
- **Support counts** `(N/M)`: N is the number of episodes whose narration names the step; M is the
  number of episodes that paint the subject. They are counted with fixed text patterns over the
  step fields, and samples of each count were read to confirm the pattern.
- **Counts are lower bounds.** Much of what is done is never said, so a low count does not weaken
  a rule. A rule is softened only by positive contrary evidence, meaning a different tool, color
  or method actually used. Example: 30 of 43 waterfall episodes paint a small fan-brush waterfall,
  so the waterfall card gives both methods. A first synthesis pass softened some rules
  on low counts alone; a review pass reverted those changes.
- **Order counts** (`05-order.md`) work differently. They compare where two subjects first appear
  in each episode, so they measure what is done, not what is said.

## Evidence classes
Every statement in the cards rests on one of three kinds of evidence:
- **stated:** said in the episode (paraphrased, with a timestamp);
- **observed:** seen in the video frames (in the studies, with the frame's timestamp);
- **inferred:** an interpretation, marked `(?)`.

## Rating weights
In `dataset/stats.md`, the `w` column weights each episode by its rating, from 0.4 to 1.6. The
rating combines IMDb (Bayesian average with a 30-vote prior) and YouTube likes (log scale), each
standardized, then averaged. Unweighted shares are shown next to the weighted ones.

## Provenance
- **Episode tables:** the two public datasets above, retrieved November 2026.
- **Ratings:** IMDb non-commercial dataset and YouTube like counts, both retrieved 6 November 2026.
- **Captions:** the official uploads' automatic English captions. 387 of 403 episodes have them.
  The dataset covers 382 of these: all 379 captioned regular episodes (of 381) and 3 guest
  episodes.
- **Models:**
  - step extraction: Claude Haiku 4.5;
  - deep studies and the accuracy audit: Claude Sonnet;
  - synthesis: Claude Opus.

  All model output is checked by code (timestamps, order, completeness) or by hand.

## Limitations
- **Captions:** automatic, with misheard words. Paint names are corrected by rule. What is not
  said aloud (angles, pressure, which brush) is often missing from the dataset.
- **Labels:** field labels are the least reliable part of the dataset (see Accuracy). Where it
  matters, check against `studies/`.
- **Deep-study selection:** 10 of the 16 episodes were chosen for mountains and water, so
  frame-checked detail (angles, positions, pressure) is richest there. Oceans, structures, night,
  moon, flowers and desert have one frame-checked study each (structures three).
- **Coverage:** the dataset is not a sample. It covers 379 of the 381 regular episodes, so its
  counts describe the series itself.
- **Ratings:** about 35 IMDb votes per episode, so noisy. IMDb favors season 1 and YouTube favors
  famous titles. Ratings only set the processing order, the weights and which variant is listed first.
- **Positions:** read from frames, ±0.05; the camera zooms and pans.
- **Scope:** this documents the method as taught on the show. It is not the only way to paint
  wet-on-wet.

## Neutrality
- Every deep-study episode was studied with the same brief, and no topic was singled out.
- Coverage limits are stated in the README.
