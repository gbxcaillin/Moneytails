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
