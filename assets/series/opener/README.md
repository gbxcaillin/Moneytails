# Money Tails opener: "The Coin Trail" clips

Round 4. Every character beat is built from chained keyframe stills (`keyframes/`, `hopper-keyframes/`) and 4 second Veo 3.1 shots pinned to a start and end frame, with a timed single-action prompt (`shots-veo/`). Kling 3 Omni versions of the same shots are kept in `shots/` and `hopper-shots/` for reference. Method in `docs/workflow.md`. `opener-rough-assembly.mp4` is a straight concat of every shot in order, silent, for review only; the real cut trims to about 25 s.

| Beat | Shot | Model | historyId | Verdict |
|---|---|---|---|---|
| 0 | `shots-veo/0-sting.mp4` | Veo 3.1 | `eMqd7U5FHN8Vdd3RE1Dg` | Pass. Coin drops into the pouch, glow flares. Kanga's real colours. |
| 1A | `shots-veo/1A-kanga-catch.mp4` | Veo 3.1 | `s8xtATopXXw5ZbZbE0J8` | Pass. Coin falls at gravity, caught cleanly in her paw. |
| 1B | `shots-veo/1B-kanga-pouch.mp4` | Veo 3.1 | `Pu7EAsbaV2eePOCIxOyM` | Pass. Coin tucked into the pouch, glow flares. |
| 1C | `shots-veo/1C-kanga-hop.mp4` | Veo 3.1 | `0KSlkzvXCxCLpI5OCcJL` | Pass. Pats pouch, looks to camera, hops off right. |
| 2A | `shots-veo/2A-maggie-snatch.mp4` | Veo 3.1 | `7yrCAIAwIdzFcCWZKRRo` (v2) | Pass. v1 dropped and re-grabbed the coin. |
| 2B | `shots-veo/2B-maggie-bag-KLING.mp4` | Kling 3 Omni | `mKMSWkXCno9c2HPNZau9` | Pass on Kling. Veo failed three times, each time dropping the coin onto the footpath beside her instead of into the bag. |
| 2C | `shots-veo/2C-maggie-run.mp4` | Veo 3.1 | `TR48jZhy3unFOZXcC8ic` (v2) | Pass. v1 spilled coins from the bag. |
| 3A | `shots-veo/3A-hopper-bounce.mp4` | Veo 3.1 | `Lt2JGcamWweeGenb6njC` (v2) | Pass. Bounce off the hat onto the bench, hat clean. v1 left a yellow mark on the hat. |
| 3B | `shots-veo/3B-hopper-pickup.mp4` | Veo 3.1 | `WTmI3JSIri8kN2IJhHfe` | Pass. Picks it up off the bench, holds it up. |
| 3B insert | `shots-veo/3B-hopper-insert.mp4` | Veo 3.1 | `3QWKGOGgeNLXggH4kGgz` (v2) | Pass. Same side of the bench, coin stays in his fingers. v1 lost the coin onto the guitar. |
| 3C | `shots-veo/3C-hopper-flick-leap.mp4` | Veo 3.1 | `zqddDKKwvOXnKXMYWWHZ` | Pass. Flick up, leap right, bench empty, coin high. |
| 4A | `shots-veo/4A-wombat-catch.mp4` | Veo 3.1 | `oYcbsQ9GkZ53DtpUEoyK` | Pass. Coin on a real arc, cap comes off under it, lands in the cap. |
| 4B | `shots-veo/4B-wombat-cap.mp4` | Veo 3.1 | `hsKwzWDiGjbanXxQzR6J` | Pass. Checks the cap, nods, cap back on. |
| 5 | `05-leap.mp4` | Kling 3 Omni | `v7cDCRGOnkP48ZGJme54` | Pass (round 2). The one group shot, kept until the end as briefed. |
| 6 | `06-title.mp4` | Kling 3 Omni | `VTt25TBriFjkedt61SA8` | Pass (round 2). |

Veo failure mode to know: when a coin has to go into a container held low on a character, Veo drops it to the ground. It handled the pouch (twice) and the cap, but not the sling bag. Rejected Veo takes are in `shots-veo/rejected/`.

## Hopper beat, take two: the flick gag in three pinned shots

The single-shot flick gag failed three times on Kling (a second coin appeared every time the model had to carry "coin on hat, then coin in hand" through one clip). Fix: split the gag into three short shots, each pinned by a start frame and an end frame generated as stills, so no clip carries the coin's state for more than about three seconds. A cut to a different angle between shots hides the joins and is normal film grammar.

| Shot | Angle | Start frame | End frame | Action | Length |
|---|---|---|---|---|---|
| 3A | Medium wide, bench left of frame | S1 strumming, no coin | S2 coin lying on bench, Hopper looking at it | Coin drops in, bounces off the hat, lands on the bench | 3 s, Kling `hFY7DVFFMy7kEWqz7YG1`. Pass: coin drops in at 1.8 s, hits the hat at 2.3 s, lies on the bench by 2.7 s, he looks down. One coin. `hopper-shots/3A-coin-bounce.mp4` |
| 3B | Medium wide, same as 3A | S2 coin on bench | S3w coin held up, shrug | He picks the coin up off the bench and holds it up | 3 s, Kling `t3Y8tAWWwcqxI7Fc4mdI`. Pass: coin on the bench until 1.5 s, then in his hand with the bench empty. `hopper-shots/3B-pickup.mp4` |
| 3B insert | Close-up, low three-quarter from the right | S3 close-up, coin in hand | none | He turns the coin, eyebrow, shrug. Optional cut-in for the angle change | 3 s, Kling `tWpBo6P1c59sTscT69y2`. Pass: coin stays in hand, he turns it and grins. `hopper-shots/3B-insert-closeup.mp4` |
| 3C | Medium wide, same as 3A | S3w wide, coin in hand ready to flick | S4 bench empty, Hopper mid-leap right, coin high | He flicks the coin up with the guitar neck and springs after it | 4 s, Kling `1aUqzEKR7gPO7qgtVu3j`. Pass: flick at 1.0 s, coin high by 1.8 s, leap from 2.4 s, bench empty, one coin. `hopper-shots/3C-flick-leap.mp4` |

Key stills live in `hopper-keyframes/` (S1 `WaWOTYQ0kKNg70L4lhRl`, S2 `mLysVBsmlWP6RpTFUjOf`, S3 close-up `T41cmZBmPUwEVJCzU9GA`, S3w `yJbLrwdYD7C7v1ilsX98`, S4 `aX9CqgNhPWj9sSqXyV05`). Seedance 2.0 single-shot comparison from S1, 6 s: `YDYuTkPJqqgFrgHlV5UP` (`hopper-shots/seedance-single-shot.mp4`). Verdict: the bounce off the hat never appears, the coin materialises in his hand, and the leap barely starts by 6 s. Not better than Kling; the pinned three-shot approach is the fix, not the model.

## Model head-to-head (round 4)

Kling's pinned shots hold continuity but the motion quality is in question, so the two hardest shots (Kanga catch K1 to K2, wombat catch W1 to W2) were re-run on three other models with the same start and end frames and a granular, timed prompt. Results in `model-test/`.

| Model | Kanga catch | Wombat catch | Per-shot cost (4 s, 720p) |
|---|---|---|---|
| PixVerse V6 | `UmNj6a25Hz9aTL2xeUWl` | `dcmYIW7tSIySryZLEUBp` | about 45 |
| Veo 3.1 fast | `s8xtATopXXw5ZbZbE0J8` | `oYcbsQ9GkZ53DtpUEoyK` | about 150 |
| Gemini Omni 1.1 Flash | `H3X1znfq9Iam7n64YGZ1` | `CHFuPGWd1EcMAInkFf8p` | about 225 |

Verdict: Veo 3.1 (fast, 720p, audio off) wins. On the wombat catch it keeps the coin visible on a real falling arc, the cap comes off under it, and the coin lands in the cap at 2 s. Gemini was close but costs half again as much and adds an audio track. PixVerse kept the coin visible but let it drift back upward mid-shot. Kling lost the coin at 0.6 s. The two passing Veo test clips are reused as shots 1A and 4A. All other pinned shots are being rebuilt on Veo into `shots-veo/`; 126 credits per 4 s shot.

Rules for the rebuild on the winning model: every clip 2 to 5 seconds, one action per clip, timing spelled out in the prompt in seconds, one character per clip until the group leap at the very end, camera static or a single slow push, start and end frames from the keyframe chain.

## Assembly order (editor)

1. `00-coin-sting` with the coin chime on the first landing.
2. `01` to `04` cut end to end. The tracking direction is left to right in every clip so the cuts read as one move. Trim each to its action endpoint.
3. `05-leap`, then a fast whip or light flash into `06-title`.
4. Overlay coin particles across the cut points if the trail needs to feel continuous.
5. Theme music under the whole thing per section 6 of the brief. Hold the title 1.5 s, hard cut to the cold open.
6. Export 1080p 16:9, then reframe for 9:16.
