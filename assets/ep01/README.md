# EP01 "The Pouch" — generated assets

Pipeline stage: **Step 1 (characters) and Step 3 (environments) first pass.** Generated on OpenArt via the MCP connector from the prompts in `episodes/ep01/openart-prompts.md`, with the global style string prefixed and the Nano Banana front-loading rule applied (`flat vector illustration, no gradients, no texture, in the style of Bluey`).

All images: Nano Banana Pro, text2image, 16:9, 1K (1376 x 768), one image per prompt. Cost was 36 credits per image after the MCP discount.

## Characters (three-view reference sheets)

| File | Character | OpenArt historyId | Review |
|---|---|---|---|
| `characters/kanga-ref-sheet.png` | KANGA | `kkKmAwhFUd47yCHCPoGW` | **Superseded.** Approved Kanga lives in `assets/series/kanga/`. This sheet is missing her green t-shirt; keep only as a record of the style test. |
| `characters/maggie-ref-sheet.png` | MAGGIE | `wgi65ab3d1ZAwh8z4Keh` | On-model. Pink and yellow sneakers, orange sling bag full of gadgets, open beak. |
| `characters/hopper-ref-sheet.png` | HOPPER | `asshHLjaqWbZmwUyv73G` | On-model. Blue bucket hat, tiny guitar, half-lidded eyes. |
| `characters/wombat-ref-sheet.png` | WOMBAT MECHANIC | `sO13cYPPxnW9ff4lsniz` | On-model. Grey overalls with oil stains, red cap, clipboard, deadpan. |

## Environments

| File | Environment | OpenArt historyId | Review |
|---|---|---|---|
| `environments/env1-main-street.png` | ENV 1 Main street | `Pg41GEUVHQ832wkYnb1X` | On-brief. Weatherboard shopfronts, corrugated awnings, sparkling electronics window, blank milk bar sign, gum trees, ocean at the end of the street. |
| `environments/env2-verandah.png` | ENV 2 Kanga's verandah | `ZrGzVsMbn0QK9rnwYNsj` | On-brief. Three mismatched chairs, potted plants, gum tree, ocean, late-afternoon light. |
| `environments/env3-explainer-space.png` | ENV 3 Explainer space | `cHYiR0lcat7vNFwOMroi` | On-brief. Empty cream backdrop, faint texture, ready for diagrams. |
| `environments/env4-roadside.png` | ENV 4 Roadside | `5hN3HLSrSmFznvT1pVxr` | On-brief. Bus stop, dunes, overcast sky, no characters. |
| `environments/env5-phone-screen.png` | ENV 5 Phone screen template | `F6oMtkLdfdudKkUWUSEI` | Usable as a UI template only. The hand holding the phone is human; regenerate as image-to-image with Kanga's sheet attached before using it for Shot 4 or Shot 15. |

## Next steps (per docs/workflow.md)

1. Characters approved and promoted to `assets/series/`. Done.
2. Storyboard generated and reviewed: `storyboard/README.md`. Done.
3. Next: video (Smart Shot for SS-1 to SS-5, image-to-video from approved panels for dialogue and explainer beats), then voices.

The OpenArt "animated series" assets folder is not reachable through the connector (it only exposes uploads, generation history and projects). The approved Kanga files from that folder were supplied by hand and live in `assets/series/kanga/`.

## Video drafts (Seedance 2.5)

| Chunk | File | historyId | Settings | Verdict |
|---|---|---|---|---|
| 01, shots 1 to 3 (0:00 to 0:30) | `video/chunk01-draft-480p-v1.mp4` | `pRMCmfTzYD9eg6EiRBrD` | 480p, 30 s, audio on, 1,629 credits. Refs: Kanga hero, Maggie, Hopper, ENV1, storyboard panels 1 to 3, Kanga voice reference `assets/series/kanga/kanga-voice-ref-opener.mp3` (upload `PhWin5XjnKXIPjtmoaDA`). Prompt in `video/chunk01-prompt-v1.md`. | Pass as a draft. Shot 1 matches panel 1 (Maggie swoop to the window, Hopper on the bench, golden light) with Kanga's voice over from 2 s. Shot 2 is the pouch silhouette with coins dropping in and the glow, no lettering. Shot 3 is the three-phone split screen revealing Maggie, Hopper and Kanga in turn with their lines and Kanga's pouch glow on the tap at 30 s. No text anywhere. Nit: the split screen sits inside a grey border rather than filling the frame; either scale it in the edit or add "panels fill the frame edge to edge" to the prompt for the 1080p pass. Voice match against the opener needs a listen. |

Method: one Seedance 2.5 element2video job per 30 s chunk, script-style prompt with shot timings and dialogue, character sheets plus environment plate plus the storyboard panels for those shots as image references, and a voice reference audio clip per speaking lead. Draft every chunk at 480p, then re-render approved chunks at 1080p with the same prompt and references.
