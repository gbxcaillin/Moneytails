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

## Seedance 2.5 clips: one complex event or two simple events per clip

A 30 s chunk with several shots and several lines gives the model too many directions and it averages them (learned on EP01 chunks 1 to 3). The unit of generation is now a clip, not a chunk:

- **One complex event, or two simple events, per clip.** A complex event is anything with a state change the viewer has to read: a character coveting the thing in the window, a transfer moving money between tiles, a balance bar being sliced, a scooter dying. A simple event is a single pose or beat with no state change: Maggie lands on the footpath, Hopper strums on the bench, Kanga sips her coffee. Two simple events can share a clip if they are in the same frame. A complex event gets a clip to itself.
- **One camera setup per clip.** No cuts inside a clip. Cuts happen in the edit.
- **One line of dialogue per clip, two at most** when it is a quick back and forth in the same frame.
- **Length is what the event needs**, usually 4 to 10 s. Never pad to fill a duration.
- **Prompt shape:** style block, character block, voice block, then a single paragraph describing the event with its timing. No shot numbers, no "cut to".
- **References:** the character sheets in the clip, the environment plate, the storyboard panel for that shot, and a voice reference for each speaking lead. Give the previous clip as a video reference only when the two clips share a setup and must match.
- **Assembly:** clips are cut together in the edit, where the on-screen text, captions and the end card are added. Draft at 480p, re-render approved clips at 1080p with the same prompt.


### Standing conventions learned on EP01 clips 01 to 13

- **Balance bars are meters, not shapes.** Describe them as a fixed outline that stays the same size, with a coloured fill inside that drains down from the right as money is spent. Never say the bar "shrinks" or "is sliced"; the model then shrinks the outline. Spending is the fill going down; a small purchase drops it a little, a big one a lot. Nothing sits inside the bar except the fill; icons of what was bought go beside the bar, never in it.
- **Insert, point-of-view and flat-graphic shots start from a checked still.** For any shot with no full character in frame (a phone in paws, a clipboard, a letter) and for any diagram or meter graphic (balance cards, the pie, pouch filling), generate the first frame with Nano Banana Pro image2image with the character sheet attached, check that the paws or hands match the sheet, then animate it with Seedance image2video and the still as `startFrame`. Text-only clip prompts get the anatomy wrong here (EP01 clip 08 came back with shaggy bear paws twice), and a storyboard panel passed as a reference anchors a graphic at the panel's small scale so the meters never render (EP01 clip 14, twice). Put every hand that will act in the still already, in its starting position; a hand that has to enter frame to tap or grab comes in as a third hand.
- **Point-of-view phone shots show only the phone and the paws holding it.** Frame it from the character's eyes: the phone fills the middle of the frame, the paws come in from the bottom corners, and the background is the ground, footpath or sky, never the character's own torso, vest or pouch. If the pouch has to glow, cut to a separate shot.
- **Wings are wings.** Maggie holds a phone with the tip of one wing and keeps the other wing as a wing, folded or spread. Never write "both wings" holding a small object and never write a flap while she holds it, or the model adds an arm.
- **Style-check every still-first start frame against the character sheet before animating.** Nano Banana Pro image2image can quietly re-render a composite in a more detailed, semi-realistic style (softer shading, lankier limbs, duller colours) that no longer matches the flat show look, and image2video then preserves that off-style clip (EP01 clip 17, three takes). When building a start frame, base it on a frame that is already in the flat style, front-load the flat-style words ("flat 2D cartoon, flat cel shading, thick uniform outlines, bright flat colours, in the style of Bluey, no gradients, no painterly detail"), attach the character's sheet, and then stack the still beside the sheet and confirm the colours, proportions, hat and outline weight match before you spend a video credit.
- **On-screen fills and slider drags go still to still.** A phone screen where a bar or slider fills, a toggle flips, or a value changes reliably only when it is bracketed: a checked start still and a checked end still, animated with Seedance image2video using both `startFrame` and `endFrame`, so the change is a clean interpolation between two known states. Prompting the fill as motion from a single still makes the model invent stray colours and speckles in the track (EP01 clip 38, first take). Say "one clean flat colour, no gradient, no stray colours" in the prompt as well.
- **Vehicles and props with a fall: state the direction and the end state.** For a ride-in or a knock-over, say which way it travels ("rides in forwards from the left, nose leading") and what it does after ("tips over and stays down; does not right itself"). Left unstated, the model may run it backwards or spring it back upright (EP01 clip 16, first take).
- **Furniture belongs to the plate.** Place benches, counters and letterboxes against something in the environment plate (the shopfront, the kerb, the window) and say "on the footpath, with the road behind", never just "on the street".

The 30 s single-pass method stays for the opener, where there is no dialogue and the beats are all one gag each.

### Prompt brief shape (from the prompt-optimizer skill, applied from EP01 clip 33)

The repo carries the prompt-optimizer skill at `.claude/skills/prompt-optimizer/` with per-model references. Use it whenever a prompt is written for OpenArt. The parts that changed our clip prompts:

- **Seedance clips are director's briefs in eight labelled parts:** FORMAT (style line), SUBJECT (who, "keeps exactly the design in image N", one job per reference), ENVIRONMENT (which plate, light), CAMERA (one setup, "the camera does not move"), ACTION written as cause then reaction with a bit of physics ("because the tap lands, the sparkle bursts and his eyebrows go up"), TIMING (seconds for each beat, then "Nothing else happens"), AUDIO (voice spec with the audio reference, lip synced line in quotes, sound effects, bed), CONSTRAINTS (positives first: "exactly two wings", "stable proportions", then the no-text line). Present tense throughout.
- **Each reference gets one stated job.** "Image 3 is the storyboard for this shot and sets the pose only" stops a panel from also setting scale or palette.
- **Negatives become positives where possible.** Nano Banana Pro and the Seedance form have no negative field, so "blank plain shapes" and "stays a wing" carry the weight; the explicit no-text line stays because it has worked every time.
- **Two-still bracketing for graphics that change state.** For a meter or diagram that fills across two clips, make the empty, part-filled and full stills as one text2image plus two image2image edits, then run each clip image2video with `startFrame` on one still and `endFrame` on the next, so the second clip starts exactly where the first ended.
- **Nano Banana Pro stills stay narrative paragraphs**, materials and layout described in prose, no keyword lists and no quality tags.
