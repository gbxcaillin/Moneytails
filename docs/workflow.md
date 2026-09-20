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
- **Dialogue video (e.g. Kanga intro):** Kling 3.0 Omni via image-to-video from the approved still. Native dialogue + lip sync + holds 2D style. Backup: generate silent in Kling, add voice with OpenArt's separate Lip Sync tool + TTS for more voice control.

## Prompting conventions
- **Global style string** (prompts/style-string.txt) prefixes every image, storyboard and video prompt, saved as an OpenArt template, identical every time:
  `2D cartoon animation style, flat cel shading, thick clean black outlines, bright saturated colours, sunny Australian coastal town, friendly children's TV aesthetic, 16:9 widescreen, no text, no watermark`
- **Negative prompt** (only where the model supports one): `3D render, realistic, photographic, blurry, extra limbs, distorted face, text, watermark, dark, gritty`
- Nano Banana ignores negative prompts and quality tags: front-load the style in positive language; if output drifts 3D/textured, add `flat vector illustration, no gradients, no texture` to the front. "In the style of Bluey" is the reliable shorthand for flat Australian 2D if needed.
- Kling video prompts: 50–150 words, one camera move per shot, action endpoints ("waves, then rests paw on pouch"), dialogue as `[Character: voice description]: "line"`, ++emphasis++ on 2–4 critical elements max.
- Character descriptions must be word-for-word identical across shots to limit drift.
- No readable text in generations; all on-screen text is added in the editor.

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
