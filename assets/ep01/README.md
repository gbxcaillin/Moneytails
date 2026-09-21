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
| 01 v2, shots 1 to 3 | `video/chunk01-draft-480p-v2.mp4` | `x5QiU0EAE3JfAXIQRTqM` | Same refs and settings as v1, prompt `video/chunk01-prompt-v2.md` (voice contrast by pitch, age and pace; animation energy block; business on every beat; split screen edge to edge), 1,629 credits. | Pass as a draft, replaces v1. Shot 1: Maggie loops in, dives, skids, hops three times, face on the glass, wipe; Hopper bobs and swings a leg. Shot 3 fills the frame; Maggie leaps and spins with wings out, Kanga shrugs, taps with a flourish, hops, pouch flares. Hopper stays lazy by design. Voice pitch estimated from the track: Kanga about 160 Hz, Maggie about 290 Hz (clearly higher), Hopper about 150 Hz (lower, but not by much). Maggie is clearly distinct; Hopper may still sit too close to Kanga and can be pushed lower next pass. Shot 1 settles after 6 s; trim to 9 s or give Maggie more business in the 1080p prompt. |
| 01 v3, shots 1 to 3 (0:00 to 0:26) | `video/chunk01-draft-480p-v3.mp4` | `3R2ruY78LX3iUfCU4hC6` | Screen time rule applied: 26 s, shot 1 cut to 8 s with one Maggie gag (face on the glass, smudge, wipe). Prompt `video/chunk01-prompt-v3.md`. 1,412 credits. | Pass, current pick. Voices: Kanga about 175 Hz, Maggie about 230 Hz, Hopper about 140 Hz. The split screen still renders inside a grey border despite "edge to edge"; scale it in the edit. |
| 02, shots 4 and 5 (0:26 to 0:56) | `video/chunk02-draft-480p-v1.mp4` | `XVXZ1dgCzRyYm5CiZegB` | Prompt `video/chunk02-prompt-v1.md`. Refs: Kanga, Maggie, Hopper, panels 4 to 7, Kanga voice. 1,629 credits. | Pass. The transfer reads as coins pouring into a money-bag tile with Kanga's pouch glowing in sync; Maggie and Hopper poke into frame for their lines. Montage carries the balance bars as briefed: Maggie's orange bar with grey ghost coins stacking, Hopper's green bar shrinking, Kanga's purple bar with the gold pouch beside it. Nits: the money-bag tile carries a dollar sign (a symbol, not a word, acceptable); Hopper's voice came out at about 175 Hz here, too close to Kanga, so cut a Hopper voice reference from chunk 3 for future chunks; a dog shop assistant appears at the counter, harmless. |
| 03, shots 6 to 8 (0:56 to 1:26) | `video/chunk03-draft-480p-v1.mp4` | `jdnvCeDRZdbzELiGa0Sc` | Prompt `video/chunk03-prompt-v1.md`. Refs: Hopper, Wombat, ENV4, panels 8 to 10. No voice ref (no Kanga). 1,629 credits. | Pass. Balance cards animate with the gold pouch card sliding up behind Kanga's; grey clouds roll over the street and the envelopes land in the letterboxes under the landlord line (about 100 Hz, dull and flat as briefed); scooter rides in, coughs, dies, wombat waddles in without looking up, clipboard, Hopper holds up the guitar. Hopper about 145 Hz. Card fill levels are small at 480p; the 1080p pass should say "fill levels large and obvious". |

Running assembly of chunks 1 to 3: `video/ep01-draft-480p-chunks01-03.mp4` (1:26).

Method: one Seedance 2.5 element2video job per 30 s chunk, script-style prompt with shot timings and dialogue, character sheets plus environment plate plus the storyboard panels for those shots as image references, and a voice reference audio clip per speaking lead. Draft every chunk at 480p, then re-render approved chunks at 1080p with the same prompt and references.

## Clips (one event per clip, current method)

| Clip | File | historyId | Settings | Verdict |
|---|---|---|---|---|
| 02, shot 1, Maggie at the window | `clips/clip02-maggie-window-480p.mp4` | `gLa8p9bnzphqb8mMv7sb` | 5 s, 480p, 300 credits. Refs: Maggie, ENV1, Kanga voice. | Pass. Every beat in the prompt is on screen in order: face flat on the glass with star-glint eyes, pull back, frantic wipe with the wing, face back on. Kanga's voice over runs under it. This is the proof that one complex event per clip is what the model wants. |
| 01, shot 1, Maggie lands, Hopper on the bench | `clips/clip01-maggie-lands-hopper-bench-480p.mp4` | `HCWCP6Be5LclsfpEDvWr` | 5 s, 480p, 300 credits. Refs: Maggie, Hopper, ENV1, panel 1, Kanga voice. | Pass. Maggie swoops in, lands, skids, turns to the window; Hopper strums on the bench throughout. Two simple events, one wide setup, clean. Kanga VO "Two mates. One payday." |
| 03 pouch title | `clips/clip03-pouch-title-480p.mp4` | `Cy4Ft4hypxJCvNXceGLk` | 4 s, 240 credits | Pass. Three coins drop, glow. |
| 04 three phones | `clips/clip04-three-phones-480p.mp4` | `K7FRspb5E8xsabxsVeE4` | 4 s | Pass. Buzz left to right, banners pop. Still carries the grey frame from panel 3; make a borderless panel 3 before the 1080p pass, or crop. |
| 05 Maggie payday | `clips/clip05-maggie-payday-480p.mp4` | `gVoE2bbC7QeV6Qjs5Zjz` (v2) | 4 s | Pass. v1 (`6asDMY8Hm3KCtHkRu1fA`, in `rejected/`) grew a third limb when she held the phone in both wings and flapped. v2: phone in one wing tip, other wing folded, three bounces. |
| 06 Hopper phone | `clips/clip06-hopper-phone-480p.mp4` | `9YS7THIeYsfi1Tipqis3` (v2) | 4 s, Hopper voice ref `assets/series/hopper/hopper-voice-ref-ep01c3.mp3` (upload `qj7nbjyaDfjcIgdphf3L`) | Pass. v1 (`dI15x7t1HggOhqsf01OX`) put the bench in the middle of the road. v2 has it on the footpath against the shopfront. Hopper about 125 Hz. |
| 07 Kanga one sec | `clips/clip07-kanga-one-sec-480p.mp4` | `8LzGSDqjhymp2PjgFB5f` | 4 s (3 s rejected, minimum is 4) | Pass. Finger up, half-smile. Kanga about 170 Hz. |
| 08 transfer | `clips/clip08-transfer-480p.mp4` | `cRMnBqaERCVQ6NqHFFjF` (v6, image2video) | 6 s | Pass. Six takes. Text-only prompts (v1 to v3) put Kanga's body behind the phone or drew shaggy bear paws. v4 and v5 started from a checked Nano Banana Pro still with both paws holding the phone, and each time the tap pulled in a third hand. v6 starts from a second still (`keyframes/clip08-pov-finger-on-screen.png`, `YI398pLBNdSrSpwasY7l`) with the left paw holding and the right finger already on the screen, so nothing has to enter frame: press, ripple, coins pour into the pouch tile, glow. Other stills in `keyframes/`. |
| 09 breakfast | `clips/clip09-breakfast-480p.mp4` | `jj3fXcQTKBftCWvNfZ3q` | 4 s | Pass. Maggie and Hopper poke in from the edges around Kanga. |
| 10 paid myself | `clips/clip10-paid-myself-480p.mp4` | `mj1N6HjEbCkAxfCFSdvO` | 5 s, both voice refs | Pass. Kanga about 160 Hz, Hopper about 115 Hz, phone into the vest pocket at the end. |
| 11 Maggie counter | `clips/clip11-maggie-counter-480p.mp4` | `rgIhYvYTVCKBOowDlXIc` | 6 s | Pass. Orange bar sliced on each tap, ghost coins stacking to four. Dog shop assistant absent this time. |
| 12 Hopper takeaway | `clips/clip12-hopper-takeaway-480p.mp4` | `Vz5L8m0WMZ6jOfKWjtyf` (v2) | 5 s | Pass. v1 shrank the whole bar; v2 describes a fixed outline with a fill that drains, and that is what renders: chips take a big chunk, each coin a little more, down to a sliver. |
| 13 Kanga coffee | `clips/clip13-kanga-coffee-480p.mp4` | `nYLC6UUeapEkRc0moQOK` (v2) | 5 s | Pass. v1 put bread slices inside the bar and barely moved it; v2 is a fixed outline whose purple fill drops one notch, gold pouch tile outside it. |

Running assembly of clips 01 to 22 (script shots 1 to 11, about 1:55): `clips/ep01-clips01-22-assembled-480p.mp4`. Batch 3 (clips 14 to 22) cost about 3,400 credits including two clip 14 retakes and two stills.

Running assembly of clips 01 to 13 (script shots 1 to 5, about 1:02): `clips/ep01-clips01-13-assembled-480p.mp4`. Batch cost about 3,300 credits, plus about 1,600 for the five retakes. Rejected takes in `clips/rejected/`. Rule added to docs/workflow.md: insert and point-of-view shots start from a checked still.
| 14 balance cards | `clips/clip14-balance-cards-480p.mp4` | `vAEqdJb4HVWzPHv2n20h` (v3, image2video) | 6 s | Pass. v1 and v2 from text prompts with panel 8 attached rendered tiny cards whose meters never moved. v3 starts from a text2image still (`keyframes/clip14-cards-full.png`, `erLwgeTR35VscDZxJ6db`): three big cards with tall full meters. Orange drains to a fifth and the red strip blinks, green drains to a sliver, purple settles at two thirds, gold pouch card slides up. |
| 15 envelopes | `clips/clip15-envelopes-480p.mp4` | `P65UT7vcGgVoNGMEMySE` | 6 s, landlord VO | Pass. Clouds roll in from the left, light dims, three envelopes land left to right. Landlord dull and flat. |
| 16 scooter dies | `clips/clip16-scooter-dies-480p.mp4` | `P6YAGulCUfVaatrdiuWJ` | 6 s | Pass. Rides in, coughs smoke, dies, tips over, Hopper nudges it. |
| 17 wombat clipboard | `clips/clip17-wombat-clipboard-480p.mp4` | `HlkMmQCxjB14lfgqmki1` | 5 s | Pass. Wombat waddles in without looking up, crouches, one tap, puff of smoke, clipboard up. |
| 18 Hopper guitar | `clips/clip18-hopper-guitar-480p.mp4` | `FR3ZCF5RlaI28UCklIVb` | 5 s, Hopper voice ref | Pass. Peers at the clipboard, swings the guitar round and offers it, wombat shrugs. |
| 19 Maggie calendar | `clips/clip19-maggie-calendar-480p.mp4` | `ZohC7YOeUirVHzkf64G7` | 6 s | Pass. Beanbag, phone in one wing tip, calendar fades in and the orange dots pop down one column. |
| 20 Kanga letter | `clips/clip20-kanga-letter-480p.mp4` | `afxVakTXvvoE73mufWfC` | 5 s, Kanga voice ref | Pass. Reads, shrugs, folds the letter, pats the pouch, glow. |
| 21 transfer back | `clips/clip21-transfer-back-480p.mp4` | `djpdjlXUHEYmGwB3khoo` (image2video) | 4 s | Pass first time using the still-first recipe: start frame `keyframes/clip21-pov-pouch-full.png` (`jZ8zRmO7yuAHZbX6ITyd`, edited from the clip 08 still). Press, coins arc from the pouch tile back to the left tile, two paws throughout. |
| 22 verandah | `clips/clip22-verandah-freaking-480p.mp4` | `r9v5Q6FEaNJKMgbv6fal` | 5 s, Hopper voice ref | Pass. Hopper and Maggie slumped, Kanga sips at the railing, Hopper lifts his head for the line. Hopper is small at frame left; fine for a wide. |

Clips 01 and 02 cut together: `clips/clips01-02-assembled-480p.mp4` (10 s). Compare with the 8 s shot 1 inside `video/chunk01-draft-480p-v3.mp4`: same beats, but every beat is now legible and in order.
