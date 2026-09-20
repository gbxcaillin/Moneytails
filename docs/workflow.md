# Production Workflow (OpenArt)

## Pipeline order (assets before scenes, always)
1. **Characters** — AI Character tool. Generate 5–10 variations, pick one, save as a named character (KANGA, MAGGIE, HOPPER, WOMBAT). Reuse the saved character in every later prompt; never retype descriptions.
2. **Turnarounds** — edit from the approved image, not fresh generation: upload the reference, prompt for front / three-quarter / side / back in a row, same outfit, colours, proportions.
3. **Environments** — save as named environments in OpenArt Worlds (main street, verandah, explainer space, roadside, phone-screen template).
4. **Storyboard** — AI Storyboard Generator, paste the shot list, attach saved characters and environments. Fix composition here; regenerate single bad panels only. Cheaper than fixing in video.
5. **Video** — in chunks of 5–10 seconds. Smart Shot for action beats (3–5 cuts per run, editable Shot Plan). Image-to-video from approved storyboard panels for dialogue and explainer beats (tighter control).
6. **Voice** — generate each character voice once, save settings, reuse. Lip sync only on medium/close shots where the mouth is visible.
7. **Assembly** — Story timeline: clips in order, voice tracks, trim, overlay real on-screen text in the editor (never generate text in-image), music bed, export 1080p 16:9.

## Model selections (decided)
- **Character stills / turnarounds:** Nano Banana Pro. Strongest at holding a reference across views. Backup: GPT Image 2. Avoid Flux/SDXL models for multi-view consistency.
- **Character style setting:** Digital Art (or Vector art). Never Photorealistic; avoid Pixar/3D since series is flat 2D. Pixar is fallback only if Digital Art comes out too painterly.
- **Pinned action shots (props changing hands, single character):** Veo 3.1 fast, image-to-video with start and end frames. Kling 3 Omni as fallback.
- **Dialogue video (e.g. Kanga intro):** Kling 3.0 Omni via image-to-video from the approved still. Native dialogue + lip sync + holds 2D style. Backup: generate silent in Kling, add voice with OpenArt's separate Lip Sync tool + TTS for more voice control.

## Prompting conventions
- **Global style string** (prompts/style-string.txt) prefixes every image, storyboard and video prompt, saved as an OpenArt template, identical every time:
  `2D cartoon animation style, flat cel shading, thick clean black outlines, bright saturated colours, sunny Australian coastal town, friendly children's TV aesthetic, 16:9 widescreen, no text, no watermark`
- **Negative prompt** (only where the model supports one): `3D render, realistic, photographic, blurry, extra limbs, distorted face, text, watermark, dark, gritty`
- Nano Banana ignores negative prompts and quality tags: front-load the style in positive language; if output drifts 3D/textured, add `flat vector illustration, no gradients, no texture` to the front. "In the style of Bluey" is the reliable shorthand for flat Australian 2D if needed.
- Kling video prompts: 50–150 words, one camera move per shot, action endpoints ("waves, then rests paw on pouch"), dialogue as `[Character: voice description]: "line"`, ++emphasis++ on 2–4 critical elements max.
- Character descriptions must be word-for-word identical across shots to limit drift.
- No readable text in generations; all on-screen text is added in the editor.
- **Screen time rule in prompts:** when writing a Seedance chunk, give character-only beats 2 to 4 seconds and spend the rest of the chunk on the concept imagery (the transfer, the pouch, the balance, the explainer). Describe the money or the mechanism as the thing that moves, with the character reacting in a line or a look. Gags are fine when they reveal a character's idiosyncrasy or play on the episode's theme; never write one in just to fill a 30 s chunk. End the chunk early and start the next one instead. Full rule in docs/series-bible.md.

## Continuity rule for any prop that changes hands (learned on the opener)

Video models cannot hold "object moves from A to B" through a single clip. Every single-shot attempt at Hopper's coin flick produced a second coin; the wombat's coin floated and shrank into his cap; Kanga and Maggie never touched theirs. The fix that works, every time so far:

1. **Generate keyframe stills first**, chained from one base image with Nano Banana Pro image-to-image ("edit the first reference and keep everything else identical, change only X"). One still per state of the prop: before, in hand, in pouch, gone. Attach the base still first and the character sheet second; the service keeps only two references.
2. **Shoot each state change as its own 3 to 4 second clip** with Veo 3.1 image-to-video (fast, 720p, audio off, about 126 credits), passing the "before" still as `startFrame` and the "after" still as `endFrame`. Write the prompt as timed beats in seconds ("0 to 1 s ..., 1 to 2.5 s ..., 2.5 to 4 s ..."), one action per beat, and say "there is only ever one coin" and "the camera does not move". Veo won a head-to-head against Kling, PixVerse and Gemini on the opener (see assets/series/opener/README.md); Kling is the fallback when Veo drops a prop to the ground.
3. **Keep every shot on the same camera side.** A closer shot is a push-in from the same angle, never a reverse. Crossing the line makes a bench or a character jump sides on the cut.
4. **Assemble the shots end to end.** A beat may run 8 to 13 seconds this way; the brief allows it.

A second model does not fix this. Seedance 2.0 failed the same single-shot gag the same way.


Round-5 additions to the rule: view the whole keyframe chain at full size before shooting and reject any drift; give the prop a physical cause (falls under gravity, motion lines) and the shortest path to the nearest large flat surface; put the catching hand on the character's open side, away from any wall; end every prop state fully inside or fully gone, and every exit shot on an empty plate; if only the last few frames drift, trim at the action endpoint instead of re-rolling.

## Credit management
- Explainer segments: stills with animated diagrams only; save video credits for character action.
- Multi-character wides drift most; budget extra attempts or stage as alternating close-ups.
- Never regenerate a whole Smart Shot sequence for one bad cut; regenerate the single cut.
- First character batches: 2 images to verify style, then scale up.

## Voice specs
- KANGA: Australian female, mid-30s, warm, unhurried, slightly amused, medium-low pitch. Never teacherly.
- MAGGIE: Australian female, 20s, fast, bright, excitable, rising sentence ends.
- HOPPER: Australian male, 20s, slow, relaxed drawl, surfer energy.
- WOMBAT: Australian male, 40s, flat deadpan.
- LANDLORD (V.O.): neutral, dull, bureaucratic.

## Seedance 2.5 single pass (learned on the opener, round 6)

For a sequence up to 30 s with several characters, one Seedance 2.5 element2video job with a script-style prompt (style block, character block with reference image numbers, audio block, then numbered shots with second ranges) beat five rounds of pinned single-action shots on every axis: continuity, motion quality, cost and time. Attach the character sheets, the environment plate and the logo as references in the order the prompt numbers them. 1080p, audio on. Reserve the pinned-keyframe method for a single prop hand-off that a one-pass render gets wrong.
