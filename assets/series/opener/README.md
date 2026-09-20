# Money Tails opener: "The Coin Trail" clips

Round 3. Every character beat is now built from chained keyframe stills (`keyframes/`, `hopper-keyframes/`) and short Kling image-to-video shots pinned to a start and end frame (`shots/`, `hopper-shots/`). Method in `docs/workflow.md`, "Continuity rule for any prop that changes hands". All clips 16:9, std resolution, sound off. `opener-rough-assembly.mp4` is a straight concat of every shot in order, 48 s raw, silent, for review only; the real cut trims to about 25 s.

| Beat | Shots | Keyframes | Review |
|---|---|---|---|
| 0 Sting | `shots/0-sting.mp4` 3 s (`shfQTJXChydJpafdcaTB`) | S1 `JI7j5sRWJbnj1LTrI0px`, S2 `Xp97rJgFxPOhRxe3dUTZ` | Pass. Kanga's real colours, coin drops into the pouch, glow flares. |
| 1 Kanga | `shots/1A-kanga-catch.mp4` (`TCTjNfSj166wmNN371L6`), `1B-kanga-pouch.mp4` (`bl1GzT46aVQA8cSOdj3S`), `1C-kanga-hop.mp4` (`mXG650fFfOjDyR4EJBO0`), 3 s each | K1 `PWLECMyaog8Vn5oN2ISN`, K2 `m06pLpZt97ueRzmLxxp1`, K3 `knMOCCQjBOwa6h3FBWV5`, K4 `X5XBjzj5JIvILOj3tRbO` | Pass. Coin falls, she catches it in her paw, tucks it into the pouch (glow flares), pats the pouch, hops off right. One coin throughout. |
| 2 Maggie | `shots/2A-maggie-snatch.mp4` (`hfGjbORbWDq4xziYOBft`), `2B-maggie-bag.mp4` (`mKMSWkXCno9c2HPNZau9`), `2C-maggie-run.mp4` (`IydhLkuxI5DCd46sfunA`), 3 s each | M1 `SlMCUcO29p6EXAOkeLKl`, M2 `1q5iZ1SmZ5crO7Y87FPp`, M3 `OnsIKOauaDiK9dRY2Lvk`, M4 `8DGKdoxiL52ZrSGN3JDT` | Pass. Swoops, snatches the coin in her beak, lands, drops it into the orange sling bag, pats the bag, runs off right. One coin throughout. |
| 3 Hopper | `hopper-shots/3A`, `3B`, `3B-insert-closeup` (same side, `sugiO1wBb4ou7Mnrvjt6`), `3C` | S1 to S4 in `hopper-keyframes/`, same-side close-up `5tzA7lubomXi3E6aBMcl` | Pass. Bounce off the hat onto the bench, pick up, close-up from the same side of the bench, flick and leap. One coin throughout. |
| 4 Wombat | `shots/4A-wombat-catch.mp4` (`ZHBCdPqRHSd5kp4JeeR7`), `4B-wombat-cap.mp4` (`fTHKnxLdnGlZ4bcZwQ19`), 3 s each | W1 `ZPlkPuZoPnGjGYFODqU6`, W2 `zCONeCwGwp4fVapXZD05`, W3 `sHkhTf3lEZPBsUTVQqlJ` | Pass with note. Coin flies in fast on a real arc and lands on top of his cap at 0.6 s; he lifts the cap off and the coin is in it; he checks, nods, puts the cap back on. Reads as "lands on his hat, he tips it into the cap" rather than a mid-air catch. If the mid-air catch is wanted, add a keyframe with the cap already held out before the coin arrives. Bear and bull scuffle throughout. |
| 5 The leap | `05-leap.mp4` 5 s (`v7cDCRGOnkP48ZGJme54`) | none | Pass (v2, Kanga hops). Unchanged from round 2. |
| 6 Title hit | `06-title.mp4` 3 s (`VTt25TBriFjkedt61SA8`) | five-tail logo still | Pass (v2, tails stay planted). Unchanged from round 2. |

Rejected versions from rounds 1 and 2 are in `rejected/` with the reason in the filename.

## Hopper beat, take two: the flick gag in three pinned shots

The single-shot flick gag failed three times on Kling (a second coin appeared every time the model had to carry "coin on hat, then coin in hand" through one clip). Fix: split the gag into three short shots, each pinned by a start frame and an end frame generated as stills, so no clip carries the coin's state for more than about three seconds. A cut to a different angle between shots hides the joins and is normal film grammar.

| Shot | Angle | Start frame | End frame | Action | Length |
|---|---|---|---|---|---|
| 3A | Medium wide, bench left of frame | S1 strumming, no coin | S2 coin lying on bench, Hopper looking at it | Coin drops in, bounces off the hat, lands on the bench | 3 s, Kling `hFY7DVFFMy7kEWqz7YG1`. Pass: coin drops in at 1.8 s, hits the hat at 2.3 s, lies on the bench by 2.7 s, he looks down. One coin. `hopper-shots/3A-coin-bounce.mp4` |
| 3B | Medium wide, same as 3A | S2 coin on bench | S3w coin held up, shrug | He picks the coin up off the bench and holds it up | 3 s, Kling `t3Y8tAWWwcqxI7Fc4mdI`. Pass: coin on the bench until 1.5 s, then in his hand with the bench empty. `hopper-shots/3B-pickup.mp4` |
| 3B insert | Close-up, low three-quarter from the right | S3 close-up, coin in hand | none | He turns the coin, eyebrow, shrug. Optional cut-in for the angle change | 3 s, Kling `tWpBo6P1c59sTscT69y2`. Pass: coin stays in hand, he turns it and grins. `hopper-shots/3B-insert-closeup.mp4` |
| 3C | Medium wide, same as 3A | S3w wide, coin in hand ready to flick | S4 bench empty, Hopper mid-leap right, coin high | He flicks the coin up with the guitar neck and springs after it | 4 s, Kling `1aUqzEKR7gPO7qgtVu3j`. Pass: flick at 1.0 s, coin high by 1.8 s, leap from 2.4 s, bench empty, one coin. `hopper-shots/3C-flick-leap.mp4` |

Key stills live in `hopper-keyframes/` (S1 `WaWOTYQ0kKNg70L4lhRl`, S2 `mLysVBsmlWP6RpTFUjOf`, S3 close-up `T41cmZBmPUwEVJCzU9GA`, S3w `yJbLrwdYD7C7v1ilsX98`, S4 `aX9CqgNhPWj9sSqXyV05`). Seedance 2.0 single-shot comparison from S1, 6 s: `YDYuTkPJqqgFrgHlV5UP` (`hopper-shots/seedance-single-shot.mp4`). Verdict: the bounce off the hat never appears, the coin materialises in his hand, and the leap barely starts by 6 s. Not better than Kling; the pinned three-shot approach is the fix, not the model.

## Assembly order (editor)

1. `00-coin-sting` with the coin chime on the first landing.
2. `01` to `04` cut end to end. The tracking direction is left to right in every clip so the cuts read as one move. Trim each to its action endpoint.
3. `05-leap`, then a fast whip or light flash into `06-title`.
4. Overlay coin particles across the cut points if the trail needs to feel continuous.
5. Theme music under the whole thing per section 6 of the brief. Hold the title 1.5 s, hard cut to the cold open.
6. Export 1080p 16:9, then reframe for 9:16.
