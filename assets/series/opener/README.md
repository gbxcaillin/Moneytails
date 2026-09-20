# Money Tails opener: "The Coin Trail" clips

All seven clips generated, reviewed and passed. Four beats were regenerated; Hopper took three passes and a gag change. OpenArt, Kling 3 Omni, 16:9, std resolution (1280x720, 24 fps), sound off (music and sound design are added in the editor per `docs/opening-sequence.md` sections 6 and 7). Character clips use element-to-video with the approved sheets and the environment plate attached; the sting and title hit use image-to-video from a still.

| Beat | File | historyId | Length | Refs | Review |
|---|---|---|---|---|---|
| 0 Sting | `00-coin-sting.mp4` | `moDiHOH2NO96QBBgo8Av` | 3 s | Panel 02 still | Pass. Coins drop in, glow pulses brighter, gentle push-in. |
| 1 Kanga | `01-kanga.mp4` | `IRDwOqai1BKdywyinAXy` | 4 s | KANGA hero, KANGA turnaround, ENV1 | Pass. Coin drifts down at the start, she pats the glowing pouch, half-smile to camera, hops off right at the end. Main street matches the plate. Took about 17 minutes to render against 2 for the others; likely the tall hero portrait reference. |
| 2 Maggie | `02-maggie.mp4` | `3k36GvDKVZlvKdH1YoPU` | 4 s | MAGGIE, ENV1 | Pass. Swoops in from top, coin in frame, lands running right with sneakers and bag on-model. |
| 3 Hopper | `03-hopper.mp4` (assembled preview) | shots in `hopper-shots/` | 13 s | S1 to S4 keyframes | Pass. The flick gag, built as four pinned shots: 3A coin bounces off the hat onto the bench, 3B he picks it up, 3B insert close-up on the coin (optional, different angle), 3C he flicks it and leaps. One coin in every frame. `03-hopper.mp4` is a straight concat of the four for preview; recut from the individual shots in the editor. Single-shot versions v1 to v4 kept in `rejected/`. |
| 4 Wombat and cameos | `04-wombat.mp4` | v2 `nfgylpFF4iFCpzy3CXHm` | 7 s | WOMBAT, ENV4 | Pass (v2). Coin arcs in from the left, he lifts the red cap and catches it without looking up, checks the cap, puts it back on, and stays in frame throughout. Bear and bull scuffle over the newspaper in the background the whole clip. v1 (4 s) kept in `rejected/`. |
| 5 The leap | `05-leap.mp4` | v2 `v7cDCRGOnkP48ZGJme54` | 5 s | KANGA hero, MAGGIE, HOPPER, ENV1 | Pass (v2). Kanga bounds upright on her hind legs, feet together, tail swinging; Maggie runs, Hopper springs; all three end big in frame with the coin trail. v1 (Kanga ran) kept in `rejected/`. |
| 6 Title hit | `06-title.mp4` | v2 `VTt25TBriFjkedt61SA8` | 3 s | Five-tail logo still | Pass (v2). Tails stay planted and only quiver, echidna spikes shake in place, lettering fixed, glow pulses, coins drift. v1 (echidna popped up) kept in `rejected/`. |

Rule: a clip runs as long as its coin gag needs. Do not cut a gag short to hit the 20 s target; trim the holds between gags instead, and let the full opener stretch toward 25 s if it has to.


## Hopper beat, take two: the flick gag in three pinned shots

The single-shot flick gag failed three times on Kling (a second coin appeared every time the model had to carry "coin on hat, then coin in hand" through one clip). Fix: split the gag into three short shots, each pinned by a start frame and an end frame generated as stills, so no clip carries the coin's state for more than about three seconds. A cut to a different angle between shots hides the joins and is normal film grammar.

| Shot | Angle | Start frame | End frame | Action | Length |
|---|---|---|---|---|---|
| 3A | Medium wide, bench left of frame | S1 strumming, no coin | S2 coin lying on bench, Hopper looking at it | Coin drops in, bounces off the hat, lands on the bench | 3 s, Kling `hFY7DVFFMy7kEWqz7YG1`. Pass: coin drops in at 1.8 s, hits the hat at 2.3 s, lies on the bench by 2.7 s, he looks down. One coin. `hopper-shots/3A-coin-bounce.mp4` |
| 3B | Medium wide, same as 3A | S2 coin on bench | S3w coin held up, shrug | He picks the coin up off the bench and holds it up | 3 s, Kling `t3Y8tAWWwcqxI7Fc4mdI`. Pass: coin on the bench until 1.5 s, then in his hand with the bench empty. `hopper-shots/3B-pickup.mp4` |
| 3B insert | Close-up, low three-quarter from the right | S3 close-up, coin in hand | none | He turns the coin, eyebrow, shrug. Optional cut-in for the angle change | 3 s, Kling `tWpBo6P1c59sTscT69y2`. Pass: coin stays in hand, he turns it and grins. `hopper-shots/3B-insert-closeup.mp4` |
| 3C | Medium wide, same as 3A | S3w wide, coin in hand ready to flick | S4 bench empty, Hopper mid-leap right, coin high | He flicks the coin up with the guitar neck and springs after it | 4 s, Kling `1aUqzEKR7gPO7qgtVu3j`. Pass: flick at 1.0 s, coin high by 1.8 s, leap from 2.4 s, bench empty, one coin. `hopper-shots/3C-flick-leap.mp4` |

Key stills live in `hopper-keyframes/` (S1 `WaWOTYQ0kKNg70L4lhRl`, S2 `mLysVBsmlWP6RpTFUjOf`, S3 close-up `T41cmZBmPUwEVJCzU9GA`, S3w `yJbLrwdYD7C7v1ilsX98`, S4 `aX9CqgNhPWj9sSqXyV05`). Seedance 2.0 single-shot comparison from S1, 6 s: `YDYuTkPJqqgFrgHlV5UP` (`hopper-shots/seedance-single-shot.mp4`). Verdict: the bounce off the hat never appears, the coin materialises in his hand, and the leap barely starts by 6 s. Not better than Kling; the pinned three-shot approach is the fix, not the model.

`opener-rough-assembly.mp4` is a straight concatenation of every clip in order at 1280x720, untrimmed and silent, 39 s. It exists only to review flow; the real cut trims each clip to its action endpoint and lands at 22 to 25 s.

## Assembly order (editor)

1. `00-coin-sting` with the coin chime on the first landing.
2. `01` to `04` cut end to end. The tracking direction is left to right in every clip so the cuts read as one move. Trim each to its action endpoint.
3. `05-leap`, then a fast whip or light flash into `06-title`.
4. Overlay coin particles across the cut points if the trail needs to feel continuous.
5. Theme music under the whole thing per section 6 of the brief. Hold the title 1.5 s, hard cut to the cold open.
6. Export 1080p 16:9, then reframe for 9:16.
